# API\_Endpoints

### **API Documentation** <a href="#api-documentation" id="api-documentation"></a>

This documentation provides a ioprehensive guide to PeoPay’s APIs, enabling developers to integrate with the PeoPay ecosystem. The APIs allow seamless access to core features such as user management, P2P payments, staking, governance, and Dynamic Contribution Scoring (DCS).

***

### **1. Overview** <a href="#overview" id="overview"></a>

PeoPay APIs enable developers to: - Authenticate users and manage accounts. - Initiate and track transactions, including crypto-to-mobile money conversions. - Access staking, rewards, and referral systems. - Participate in governance through voting and proposal submission. - Monitor user contributions and penalties via DCS.

#### **Base URL** <a href="#base-url" id="base-url"></a>

* **Production Environment**: `https://api.peopay.io/v1`
* **Sandbox Environment**: `https://sandbox.api.peopay.io/v1`

***

### **2. Authentication** <a href="#authentication" id="authentication"></a>

#### **Endpoint: Login** <a href="#endpoint-login" id="endpoint-login"></a>

Authenticate users and retrieve a session token for subsequent API requests.

* **Method**: `POST`
* **URL**: `/auth/login`

**Request**

```
{
  "username": "user@example.io",
  "password": "securePassword123"
}
```

**Response**

```
{
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "expires_in": 3600
}
```

***

#### **Endpoint: Register** <a href="#endpoint-register" id="endpoint-register"></a>

Create a new user account.

* **Method**: `POST`
* **URL**: `/auth/register`

**Request**

```
{
  "username": "user@example.io",
  "password": "securePassword123",
  "mobile_number": "+1234567890"
}
```

**Response**

```
{
  "message": "User registered successfully. Please verify your email."
}
```

***

### **3. User Management** <a href="#user-management" id="user-management"></a>

#### **Endpoint: Get User Profile** <a href="#endpoint-get-user-profile" id="endpoint-get-user-profile"></a>

Retrieve user details, including DCS score and staking status.

* **Method**: `GET`
* **URL**: `/user/profile`
* **Headers**: `Authorization: Bearer <token>`

**Response**

```
{
  "username": "user@example.io",
  "mobile_number": "+1234567890",
  "dcs_score": 1250,
  "staking_balance": 500,
  "referrals": 10
}
```

***

### **4. Transactions** <a href="#transactions" id="transactions"></a>

#### **Endpoint: Send P2P Payment** <a href="#endpoint-send-p2p-payment" id="endpoint-send-p2p-payment"></a>

Send a peer-to-peer payment using PeoCoin.

* **Method**: `POST`
* **URL**: `/transactions/p2p`

**Request**

```
{
  "recipient": "recipient@example.io",
  "amount": 50,
  "message": "Payment for services"
}
```

**Response**

```
{
  "transaction_id": "abc123",
  "status": "success",
  "timestamp": "2024-01-01T12:00:00Z"
}
```

***

#### **Endpoint: Crypto-to-Mobile Conversion** <a href="#endpoint-crypto-to-mobile-conversion" id="endpoint-crypto-to-mobile-conversion"></a>

Convert crypto to mobile money.

* **Method**: `POST`
* **URL**: `/transactions/convert`

**Request**

```
{
  "amount": 100,
  "currency": "PEO",
  "mobile_number": "+1234567890"
}
```

**Response**

```
{
  "conversion_id": "conv123",
  "status": "processing",
  "mobile_money_balance": 1000,
  "exchange_rate": 1.2
}
```

***

### **5. Staking** <a href="#staking" id="staking"></a>

#### **Endpoint: Stake PeoCoin** <a href="#endpoint-stake-peocoin" id="endpoint-stake-peocoin"></a>

Stake PeoCoin to earn rewards.

* **Method**: `POST`
* **URL**: `/staking/stake`

**Request**

**Response**

```
{
  "staking_id": "stake123",
  "status": "success",
  "message": "You have successfully staked 200 PEO."
}
```

***

#### **Endpoint: Get Staking Rewards** <a href="#endpoint-get-staking-rewards" id="endpoint-get-staking-rewards"></a>

Retrieve current staking rewards.

* **Method**: `GET`
* **URL**: `/staking/rewards`
* **Headers**: `Authorization: Bearer <token>`

**Response**

```
{
  "total_rewards": 50,
  "next_payout": "2024-01-15T00:00:00Z"
}
```

***

### **6. Governance** <a href="#governance" id="governance"></a>

#### **Endpoint: Submit Proposal** <a href="#endpoint-submit-proposal" id="endpoint-submit-proposal"></a>

Submit a governance proposal.

* **Method**: `POST`
* **URL**: `/governance/proposals`

**Request**

```
{
  "title": "Proposal to Increase Staking Yields",
  "description": "This proposal suggests increasing staking yields by 5% to encourage participation.",
  "category": "Staking",
  "attachments": []
}
```

**Response**

```
{
  "proposal_id": "prop123",
  "status": "submitted",
  "message": "Your proposal has been submitted for review."
}
```

***

#### **Endpoint: Vote on Proposal** <a href="#endpoint-vote-on-proposal" id="endpoint-vote-on-proposal"></a>

Cast a vote on an active proposal.

* **Method**: `POST`
* **URL**: `/governance/vote`

**Request**

```
{
  "proposal_id": "prop123",
  "vote": "yes"
}
```

**Response**

```
{
  "status": "success",
  "message": "Your vote has been recorded."
}
```

***

### **7. Dynamic Contribution Scoring (DCS)** <a href="#dynamic-contribution-scoring-dcs" id="dynamic-contribution-scoring-dcs"></a>

#### **Endpoint: Get DCS Score** <a href="#endpoint-get-dcs-score" id="endpoint-get-dcs-score"></a>

Retrieve the user’s DCS score.

* **Method**: `GET`
* **URL**: `/dcs/score`
* **Headers**: `Authorization: Bearer <token>`

**Response**

```
{
  "dcs_score": 1350,
  "breakdown": {
    "transactions": 600,
    "staking": 500,
    "governance": 200,
    "referrals": 50,
    "penalties": -50
  }
}
```

***

### **8. Error Codes** <a href="#error-codes" id="error-codes"></a>

#### **iomon Errors** <a href="#iomon-errors" id="iomon-errors"></a>

| **Error Code** | **Message**             | **Description**                          |
| -------------- | ----------------------- | ---------------------------------------- |
| 400            | `Bad Request`           | Invalid or malformed request data.       |
| 401            | `Unauthorized`          | Missing or invalid authentication token. |
| 403            | `Forbidden`             | Insufficient permissions.                |
| 404            | `Not Found`             | Requested resource does not exist.       |
| 500            | `Internal Server Error` | An unexpected error occurred.            |

***

### **9. Rate Limits** <a href="#rate-limits" id="rate-limits"></a>

* **Free Tier**: 100 requests per minute.
* **Pro Tier**: 500 requests per minute.
*   Rate limit status is returned in the headers:

    ```
    X-RateLimit-Limit: 100
    X-RateLimit-Remaining: 80
    X-RateLimit-Reset: 1683721200
    ```

***

### **10. Examples** <a href="#examples" id="examples"></a>

#### **Send a Payment (cURL)** <a href="#send-a-payment-curl" id="send-a-payment-curl"></a>

```
curl -X POST https://api.peopay.io/v1/transactions/p2p \
-H "Authorization: Bearer <token>" \
-H "Content-Type: application/json" \
-d '{
  "recipient": "recipient@example.io",
  "amount": 50,
  "message": "Payment for services"
}'
```

***

#### **Next Steps** <a href="#next-steps" id="next-steps"></a>

1. Test API endpoints in the sandbox environment.
2. Follow our Developer Guide for integration tutorials.
3. Join our iomunity forum for support.
