# TPRO Documentation

## Description

This repository contains official documentation for TPRO project. We recommend you to read this pages on [official website](https://tpro.pro/docs). If you see any problems or misleading parts of this document, tell use about it in [Github Issues](https://github.com/tpro-network/docs/issues) or consider making contributions yourself.

## Table of Contents

- [Abstract](abstract.md)
- [Introduction](introduction.md)
- [Objectives and Design Considerations](objectives-and-design-considerations.md)
    - [Design Considerations](objectives-and-design-considerations.md#design-considerations)
        - [Delegation of Processing Power](objectives-and-design-considerations.md#delegation-of-processing-power)
        - [Delegation of storage](objectives-and-design-considerations.md#delegation-of-storage)
        - [Data providers vs resource providers domain gap](objectives-and-design-considerations.md#data-providers-vs-resource-providers)
        - [TPRO at the center](objectives-and-design-considerations.md#tpro-at-the-center)
        - [File sizes](objectives-and-design-considerations.md#file-sizes)
        - [Replication](objectives-and-design-considerations.md#replication)
        - [On-chain reporting](objectives-and-design-considerations.md#on-chain-reporting)
    - [Design Overview](objectives-and-design-considerations.md#design-overviewdesign-overview)
        - [TPRO network overview](objectives-and-design-considerations.md#tpro-network-overview)
    - [Design Objectives](objectives-and-design-considerations.md#design-objectives)
- [Proposed Solutions](proposed-solutions.md)
    - [Models](proposed-solutions.md#models)
        - [Publishing model scheme](proposed-solutions.md#models-schemes-publishing)
        - [Retrieving model scheme](proposed-solutions.md#models-schemes-retrieving)
        - [Publishing model instance](proposed-solutions.md#models-publishing)
        - [Storing model instance](proposed-solutions.md#models-storing)
        - [Previewing model instance](proposed-solutions.md#models-previewing)
        - [Purchasing model instance](proposed-solutions.md#models-purchasing)
    - [Tokenomics](proposed-solutions.md#tokenomics)
        - [Publishing tokenomics scheme](proposed-solutions.md#tokenomics-schemes-publishing)
        - [Retrieving tokenomics schehme](proposed-solutions.md#tokenomics-schemes-retrieving)
        - [Publishing tokenomics instance](proposed-solutions.md#tokenomics-publishing)
        - [Storing tokenomics instance](proposed-solutions.md#tokenomics-storing)
        - [Previewing tokenomics instance](proposed-solutions.md#tokenomics-previewing)
    - [Simulations](proposed-solutions.md#simulations)
        - [Performing simulation](proposed-solutions.md#simulations-performing)
        - [Publishing simulation results](proposed-solutions.md#simulations-publishing)
        - [Storing simulation results](proposed-solutions.md#simulations-storing)
        - [Previewing simulation results](proposed-solutions.md#simulations-previewing)
        - [Purchasing simulation results](proposed-solutions.md#simulations-purchasing)
    - [Analysis Reports](proposed-solutions.md#analysis-reports)
    - [Lifetime Events](proposed-solutions.md#lifetime-events)
    - [Rewarding](proposed-solutions.md#rewarding)
        - [Rewarding model providers](proposed-solutions.md#rewarding-model-providers)
        - [Rewarding tokenomics providers](proposed-solutions.md#rewarding-tokenomics-providers)
        - [Rewarding simulation operators](proposed-solutions.md#rewarding-simulation-operators)
        - [Rewarding analysts](proposed-solutions.md#rewarding-analysts)
        - [Rewarding storage providers](proposed-solutions.md#rewarding-storage-providers)
        - [Rewarding processing providers](proposed-solutions.md#rewarding-processing-providers)
        - [Rewarding TPRO](proposed-solutions.md#rewarding-tpro)
        - [Further incentivization](proposed-solutions.md#further-incentivization)
    - [Proofs](proposed-solutions.md#proofs)
        - [Proof of Offer (PoO)](proposed-solutions.md#proofs-poo)
        - [Proof of Storage (PoS)](proposed-solutions.md#proofs-pos)
        - [Proof of Purchase (PoP)](proposed-solutions.md#proofs-pop)
        - [Proof of Simulation (PoSIM)](proposed-solutions.md#proofs-posim)
- [Managing Risks](manging-risks.md)
    - [Lack of adoption](manging-risks.md#lack-of-adoption)
    - [Unfair rewarding](manging-risks.md#unfair-rewarding)
    - [Unfair randomness](manging-risks.md#unfair-randomness)
    - [Lack of permament storage](manging-risks.md#lack-of-permament-storage)
    - [Repackaging instances](manging-risks.md#repackaging-instances)
    - [Pirating instances](manging-risks.md#pirating-instances)
    - [Defective uptime](manging-risks.md#defective-uptime)
- [Economic Simulations](economic-simulations.md)
  - [Form](economic-simulations.md#form)
      - [Project Selection](economic-simulations.md#1_project_selection)
      - [Liquidity Configuration](economic-simulations.md#2_liquidity_configuration)
      - [Allocation Rounds and Vesting](economic-simulations.md#3_allocation_rounds_and_vesting)
      - [Supply Strategy Configuration](economic-simulations.md#4_supply_strategy_configuration)
      - [Secondary Market Configuration](economic-simulations.md#5_secondary_market_configuration)
  - [Simulations](economic-simulations.md#simulations)
      - [Simulation Step](economic-simulations.md#simulation_step)
        - [Randomness Within the Scenario](economic-simulations.md#randomness_within_the_scenario)
        - [DEX](economic-simulations.md#dex)
        - [CEX](economic-simulations.md#cex)
        - [Vesting](economic-simulations.md#vesting)
    - [Primary Market Strategies](economic-simulations.md#primary_market_strategies)
        - [Random Sale](economic-simulations.md#random_sale)
        - [Aggressive Random Sale](economic-simulations.md#aggressive_random_sale)
        - [Incremental Doubling Sales](economic-simulations.md#incremental_doubling_sales)
        - [Extended Profit Multiplier](economic-simulations.md#extended_profit_multiplier)
        - [Incremental Profit Doubling](economic-simulations.md#incremental_profit_doubling)
    - [Secondary Market Agents](economic-simulations.md#secondary_market_agents)
        - [Base Agent](economic-simulations.md#base_agent)
        - [Low Advanced](economic-simulations.md#low_advanced)
        - [Moderately Advanced](economic-simulations.md#moderately_advanced)
        - [Very Advanced](economic-simulations.md#very_advanced)
        - [Speculator](economic-simulations.md#speculator)
  - [Scoring Engine](economic-simulations.md#scoring_engine)
      - [Allocations](economic-simulations.md#allocations)
      - [Demand](economic-simulations.md#demand)
      - [Availability](economic-simulations.md#availability)
      - [Short-term Price](economic-simulations.md#short_term_price)
      - [Long-term Price](economic-simulations.md#long_term_price)
      - [Additional Metrics](economic-simulations.md#additional_metrics)
    - [Detailed Results of the Simulation](economic-simulations.md#detailed_results_of_the_simulation)
- [$TPRO Pool](pool.md)
  - [Liquidity Pool](pool.md#balancer_pool)
  - [Dynamic Fee](pool.md#dynamic_fee)
    - [Mechanism Parameters](pool.md#mechanism_parameters_dynamic_fee)
    - [Mechanisms Mathematical Specification](pool.md#mechanism_mathematical_specification_dynamic_fee)
  - [Impermanent Loss Protection Mechanism](pool.md#impermanent_loss_protection)
    - [Mechanism Parameters](pool.md#impermanent_loss_protection_machnism_parameters)
    - [Mechanisms Mathematical Specification](pool.md#impermanent_loss_protection_mathematical_specification)
## Contributing

For contributions submitting documentation for the **current stable release**, submit it to the corresponding branch. For example, documentation for `TPRO 0.3` should be submitted to the `0.3` branch. Documentation intended for the upcoming release should be submitted to the master branch.
