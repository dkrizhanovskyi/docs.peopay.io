---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Tokenomics and Economic Framework for PeoPay

### **1. Overview**

PeoCoin (PEO) serves as the foundational utility and governance token within the PeoPay ecosystem. This document presents a comprehensive tokenomics model designed to ensure long-term sustainability, incentivize active ecosystem participation, and align with PeoPay’s overarching vision of financial inclusion. The model combines deflationary mechanisms, staking rewards, and milestone-based unlocks to stabilize token value while fostering ecosystem expansion. Furthermore, it incorporates dynamic mechanisms that enable adaptability to market fluctuations and evolving user needs.

The PeoPay ecosystem is strategically engineered to bridge gaps in financial inclusion by leveraging blockchain technology’s inherent transparency, security, and efficiency. By addressing the challenges faced by underbanked populations, the framework ensures scalability and governance transparency while promoting ecosystem resilience through decentralized governance structures.

***

### **2. Total Token Supply**

* **Elastic Supply**: Initially set at 1,000,000,000 PEO, the supply is governed through a community-driven approach that allows for dynamic adjustments. These adjustments are guided by detailed economic modeling and require stakeholder approval, ensuring equitable and data-driven decisions.
  * **Adjustment Mechanisms**:
    * **Expansion**: Supply increases may be introduced to accommodate growing transactional volumes or to support emerging market integrations.
    * **Contraction**: Supply reductions are considered during periods of oversaturation to preserve token value and deflationary pressure.
* **Blockchain Infrastructure**: Initially deployed on Polygon for scalability and cost efficiency, PeoPay plans future integrations with Ethereum, Solana, and other high-performance blockchains to foster cross-chain interoperability and expand liquidity options.
  * **Rationale**:
    * Polygon’s low transaction costs and high throughput provide an optimal launch environment.
    * Cross-chain expansion enhances ecosystem accessibility, ensuring broader participation and seamless integration with decentralized finance (DeFi) protocols.

***

### **3. Token Allocation**

#### **Detailed Token Allocation Overview**

<table data-header-hidden><thead><tr><th width="190"></th><th></th><th></th><th></th></tr></thead><tbody><tr><td><strong>Category</strong></td><td><strong>Allocation (%)</strong></td><td><strong>Amount (PEO)</strong></td><td><strong>Vesting/Unlock Criteria</strong></td></tr><tr><td>Ecosystem Growth</td><td>15%</td><td>150,000,000</td><td>Quarterly allocations contingent upon achieving a 5% growth in active users, with adjustments for high-growth regions. Allocations will fund regional marketing, user onboarding initiatives, and partnerships to promote financial literacy in underserved areas.</td></tr><tr><td>Staking Rewards</td><td>15%</td><td>150,000,000</td><td>Distributed over a 10-year period, dynamically aligned with staking pool growth and overall ecosystem activity. Participants providing liquidity in high-demand trading pairs are eligible for additional rewards proportional to their contributions.</td></tr><tr><td>Team &#x26; Advisors</td><td>10%</td><td>100,000,000</td><td>Subject to a 1-year cliff and linear vesting over 3 years, tied to achieving roadmap milestones verified through community audits. Performance-based bonuses incentivize exceptional contributions to ecosystem development and governance initiatives.</td></tr><tr><td>Reserves &#x26; Liquidity</td><td>20%</td><td>200,000,000</td><td>Reserved for liquidity stabilization, market interventions, and infrastructure upgrades. A contingency fund is included to mitigate unforeseen events, with all expenditures subject to governance approvals to maintain transparency and accountability.</td></tr><tr><td>Private Investors</td><td>20%</td><td>200,000,000</td><td>Allocated via structured private sales under Fair Token Offering (FTO) principles. Tranches are tailored to attract institutional investors and high-net-worth individuals while ensuring fairness and accessibility for smaller participants.</td></tr><tr><td>ICO and CEX Listings</td><td>10%</td><td>100,000,000</td><td>Aimed at increasing accessibility through Initial Coin Offerings and listings on major centralized exchanges. Funds will also cover integrations with mobile payment platforms and regional promotional campaigns to enhance adoption in emerging markets.</td></tr><tr><td>Innovation &#x26; Development</td><td>10%</td><td>100,000,000</td><td>Directed toward research and development, pilot programs, and the deployment of new protocols. Collaboration with academic institutions and technology providers ensures continuous innovation and relevance within the rapidly evolving blockchain landscape.</td></tr></tbody></table>

***

### **4. Mathematical Implementation**

#### **1. Ecosystem Growth Allocation**

*   **Quarterly Release Formula**:

    $$
    Qa=Sg16if Growth Rate (GR)≥5%Q_a = \frac{S_g}{16} \quad \text{if Growth Rate (GR)} \geq 5\%
    $$

    Where:

    * QaQ\_a: Quarterly Allocation.
    * SgS\_g: Total allocation for Ecosystem Growth (150,000,000 PEO).
*   **Regional Adjustment Formula**:

    $$
    Qr=Qa×(1+GRr−GRg100)Q_r = Q_a \times \left(1 + \frac{GR_r - GR_g}{100}\right)
    $$

    Where:

    * QrQ\_r: Adjusted allocation for a specific region.
    * GRrGR\_r: Regional Growth Rate.
    * GRgGR\_g: Global Growth Target.

#### **2. Staking Rewards**

*   **Dynamic Yield Formula**:

    $$
    Rt=Rb×(1+GRs100)R_t = R_b \times \left(1 + \frac{GR_s}{100}\right)
    $$

    Where:

    * RtR\_t: Total rewards for the staking period.
    * RbR\_b: Base reward amount.
    * GRsGR\_s: Growth Rate of Staking Pools.
*   **Liquidity Bonus Formula**:

    $$
    Bt=Rt×M×LB_t = R_t \times M \times L
    $$

    Where:

    * BtB\_t: Bonus for liquidity contributions.
    * MM: Bonus Multiplier (based on market demand).
    * LL: Liquidity contribution percentage.

#### **3. Team and Advisor Vesting**

* **Vesting Formula**:

Where:

$$
Va=St3×McMtV_a = \frac{S_t}{3} \times \frac{M_c}{M_t}
$$

* VaV\_a: Annual vesting amount.
* StS\_t: Total team allocation.&#x20;
* McM\_c: Completed milestones.&#x20;
* MtM\_t: Total milestones.

***

**5. Summary**

The PeoPay tokenomics framework is a sophisticated model designed to ensure equitable growth, economic sustainability, and long-term ecosystem resilience. Through adaptive supply mechanisms, performance-driven staking rewards, and robust governance structures, PeoPay aligns the interests of all stakeholders. By integrating regional strategies and promoting inclusivity, the ecosystem is positioned to lead in addressing financial inclusion challenges while fostering global adoption of decentralized technologies.
