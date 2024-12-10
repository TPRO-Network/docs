# GraphQL Schema

## Assumptions



| Field | Type | Description |
|-------|------|-------------|
| dex | String |  |
| cex | String |  |
| vesting | String |  |
| disclaimer | String |  |
| others | String |  |

## String

The `String` scalar type represents textual data, represented as UTF-8 character sequences. The String type is most often used by GraphQL to represent free-form human-readable text.


## SocialEntry



| Field | Type | Description |
|-------|------|-------------|
| name | String |  |
| data | String |  |

## Project



| Field | Type | Description |
|-------|------|-------------|
| slug | String! |  |
| symbol | String |  |
| name | String |  |
| averageScore | Float |  |
| assumptions | Assumptions |  |
| logo | String |  |
| sources | \[String] |  |
| website | String |  |
| socials | \[SocialEntry] |  |
| createdAt | Int |  |
| updatedAt | Int |  |

## Float

The `Float` scalar type represents signed double-precision fractional values as specified by [IEEE 754](https://en.wikipedia.org/wiki/IEEE_floating_point).


## Int

The `Int` scalar type represents non-fractional signed whole numeric values. Int can represent values between -(2^31) and 2^31 - 1.


## AgentsParams



| Field | Type | Description |
|-------|------|-------------|
| base_agent_dollars | Int |  |
| base_agent_sale_percentage | Float |  |
| sum_dollars_other_agents | Int |  |

## SimulationShort



| Field | Type | Description |
|-------|------|-------------|
| id | String |  |
| execution_time_seconds | Int |  |
| agents | \[String] |  |
| agents_params | AgentsParams |  |
| liquidity_reserve | String |  |
| liquidity_tokens | String |  |
| score | Float |  |
| createdAt | Int |  |

## Agent



| Field | Type | Description |
|-------|------|-------------|
| name | String |  |
| data | \[[String]] |  |

## MetricEntry



| Field | Type | Description |
|-------|------|-------------|
| name | String |  |
| data | \[[Float]] |  |

## Metric



| Field | Type | Description |
|-------|------|-------------|
| median | MetricEntry |  |
| average | MetricEntry |  |
| range | MetricEntry |  |

## Strategy



| Field | Type | Description |
|-------|------|-------------|
| name | String |  |
| data | Float |  |

## Pool



| Field | Type | Description |
|-------|------|-------------|
| name | String |  |
| data | \[Strategy] |  |

## MetricsData



| Field | Type | Description |
|-------|------|-------------|
| percentage_timesteps_above_listing_price | Float |  |
| min_price | Float |  |
| market_cap_for_min_price | Float |  |
| max_price | Float |  |
| market_cap_for_max_price | Float |  |
| increase_timesteps_percentage | Float |  |
| price_below_25 | Float |  |
| price_above_50 | Float |  |
| longest_increase_trend | Int |  |
| longest_decrease_trend | Int |  |
| price_change_24h | Float |  |
| price_change_7d | Float |  |
| price_change_30d | Float |  |
| price_change_180d | Float |  |
| price_change_365d | Float |  |
| price_change_max | Float |  |

## VestingStackedArea



| Field | Type | Description |
|-------|------|-------------|
| vesting_data | \[MetricEntry] |  |
| extra_line | MetricEntry |  |

## TokenPoolDataset



| Field | Type | Description |
|-------|------|-------------|
| name | String |  |
| data | \[Float] |  |
| unit | String |  |
| type | String |  |
| valueDecimals | Int |  |

## LiquidityPools



| Field | Type | Description |
|-------|------|-------------|
| xData | \[Int] |  |
| datasets | \[TokenPoolDataset] |  |

## ScoringData



| Field | Type | Description |
|-------|------|-------------|
| main_score | Float |  |
| average_score | \[Int] |  |
| categories | \[String] |  |

## TokenPriceMonths



| Field | Type | Description |
|-------|------|-------------|
| name | String |  |
| data | \[Int] |  |

## TokenPriceAverageTokenPrice



| Field | Type | Description |
|-------|------|-------------|
| name | String |  |
| data | \[Float] |  |

## TokenPriceAverageSoldTokens



| Field | Type | Description |
|-------|------|-------------|
| name | String |  |
| data | \[Int] |  |

## TokenPriceAverageBoughtTokens



| Field | Type | Description |
|-------|------|-------------|
| name | String |  |
| data | \[Int] |  |

## TokenPriceWithSupplyAndDemand



| Field | Type | Description |
|-------|------|-------------|
| months | TokenPriceMonths |  |
| average_token_price | TokenPriceAverageTokenPrice |  |
| average_sold_tokens | TokenPriceAverageSoldTokens |  |
| average_bought_tokens | TokenPriceAverageBoughtTokens |  |

## UnvestedVestedClaimedSoldRoundData



| Field | Type | Description |
|-------|------|-------------|
| unvested_tokens | \[Int] |  |
| vested_tokens | \[Int] |  |
| claimed_tokens | \[Int] |  |
| sold_tokens | Metric |  |

## UnvestedVestedClaimedSoldRound



| Field | Type | Description |
|-------|------|-------------|
| name | String |  |
| data | UnvestedVestedClaimedSoldRoundData |  |

## MarketDataset



| Field | Type | Description |
|-------|------|-------------|
| name | String |  |
| data | \[Float] |  |
| unit | String |  |
| type | String |  |
| valueDecimals | Int |  |

## SecondaryMarketCumulative



| Field | Type | Description |
|-------|------|-------------|
| xData | \[Int] |  |
| datasets | \[MarketDataset] |  |

## Simulation



| Field | Type | Description |
|-------|------|-------------|
| id | String |  |
| execution_time_seconds | Int |  |
| agents | \[String] |  |
| agents_params | AgentsParams |  |
| liquidity_reserve | String |  |
| liquidity_tokens | String |  |
| score | Float |  |
| sold_individual_agent | \[Agent] |  |
| bought_individual_agent | \[Agent] |  |
| tokens_bought_metric | Metric |  |
| fully_diluted_valuation | Metric |  |
| volume | Metric |  |
| market_cap | Metric |  |
| cumulative_sold_primary_market | Metric |  |
| token_price | Metric |  |
| primary_market_profits | Metric |  |
| min_needed_demand | Metric |  |
| tokens_sold_metric | Metric |  |
| strategies_profits | \[Pool] |  |
| metrics | MetricsData |  |
| primary_market_sold_scatter_plot | \[MetricEntry] |  |
| vesting_stacked_area | VestingStackedArea |  |
| liquidity_pools | LiquidityPools |  |
| scoring | ScoringData |  |
| token_price_with_supply_and_demand | TokenPriceWithSupplyAndDemand |  |
| unvested_vested_claimed_sold | \[UnvestedVestedClaimedSoldRound] |  |
| secondary_market_cumulative | SecondaryMarketCumulative |  |
| createdAt | Int |  |

## GetProjectsOutput



| Field | Type | Description |
|-------|------|-------------|
| projects | \[Project] |  |
| nextToken | String |  |

## GetSimulationsOutput



| Field | Type | Description |
|-------|------|-------------|
| simulations | \[SimulationShort] |  |
| nextToken | String |  |

## ProjectInfoDexSettingsInput



| Field | Type | Description |
|-------|------|-------------|
| reserve | Int |  |
| tokens | Int |  |
| listing_price | Float |  |

## ProjectInfoCexSettingsInput



| Field | Type | Description |
|-------|------|-------------|
| market_maker_dollars | Int |  |
| market_maker_tokens | Int |  |
| listing_price | Float |  |

## ProjectInfoInput



| Field | Type | Description |
|-------|------|-------------|
| project_name | String! |  |
| project_symbol | String! |  |
| project_slug | String! |  |
| number_of_timesteps | Int! |  |
| timestep_duration | String! |  |
| dex | Boolean! |  |
| dex_settings | ProjectInfoDexSettingsInput |  |
| cex | Boolean! |  |
| cex_settings | ProjectInfoCexSettingsInput |  |

## Boolean

The `Boolean` scalar type represents `true` or `false`.


## PrimaryMarketRoundSupplyStrategiesInput



| Field | Type | Description |
|-------|------|-------------|
| strategy_random | Boolean! |  |
| strategy_random_aggressive | Boolean! |  |
| strategy_1 | Boolean! |  |
| strategy_2 | Boolean! |  |
| strategy_3 | Boolean! |  |

## PrimaryMarketRoundInput



| Field | Type | Description |
|-------|------|-------------|
| name | String! |  |
| type | String! |  |
| number_of_tokens | String! |  |
| tge_percentage | Float! |  |
| cliff | Int! |  |
| vesting | Int! |  |
| buy_price | Float! |  |
| supply_strategies | PrimaryMarketRoundSupplyStrategiesInput! |  |

## PrimaryMarketInput



| Field | Type | Description |
|-------|------|-------------|
| primary_market_rounds | \[PrimaryMarketRoundInput!] |  |

## SecondaryMarketAgentsInput



| Field | Type | Description |
|-------|------|-------------|
| base_agent | Boolean! |  |
| low_advanced | Boolean! |  |
| moderately_advanced | Boolean! |  |
| very_advanced | Boolean! |  |
| speculator | Boolean! |  |

## SecondaryMarketAgentsParamsInput



| Field | Type | Description |
|-------|------|-------------|
| base_agent_dollars | Int |  |
| base_agent_sale_percentage | Float |  |
| sum_dollars_other_agents | Int |  |

## SecondaryMarketInput



| Field | Type | Description |
|-------|------|-------------|
| agents | SecondaryMarketAgentsInput! |  |
| agents_params | SecondaryMarketAgentsParamsInput |  |

## AssumptionsInput



| Field | Type | Description |
|-------|------|-------------|
| dex | String |  |
| cex | String |  |
| vesting | String |  |
| disclaimer | String |  |
| others | String |  |

## SocialEntryInput



| Field | Type | Description |
|-------|------|-------------|
| name | String! |  |
| data | String! |  |

## CreateSimulationInput



| Field | Type | Description |
|-------|------|-------------|
| name | String! |  |
| info | ProjectInfoInput! |  |
| primary_market | PrimaryMarketInput! |  |
| secondary_market | SecondaryMarketInput! |  |
| assumptions | AssumptionsInput |  |
| logo | String! |  |
| sources | \[String!] |  |
| website | String |  |
| socials | \[SocialEntryInput!] |  |

## PrimaryMarketRoundSupplyStrategies



| Field | Type | Description |
|-------|------|-------------|
| strategy_random | Boolean |  |
| strategy_random_aggressive | Boolean |  |
| strategy_1 | Boolean |  |
| strategy_2 | Boolean |  |
| strategy_3 | Boolean |  |

## PrimaryMarketRound



| Field | Type | Description |
|-------|------|-------------|
| name | String! |  |
| type | String! |  |
| number_of_tokens | String! |  |
| tge_percentage | Float! |  |
| cliff | Int! |  |
| vesting | Int! |  |
| buy_price | Float |  |
| supply_strategies | PrimaryMarketRoundSupplyStrategies |  |

## PrimaryMarket



| Field | Type | Description |
|-------|------|-------------|
| primary_market_rounds | \[PrimaryMarketRound!] |  |

## SecondaryMarketAgents



| Field | Type | Description |
|-------|------|-------------|
| base_agent | Boolean! |  |
| low_advanced | Boolean! |  |
| moderately_advanced | Boolean! |  |
| very_advanced | Boolean! |  |
| speculator | Boolean! |  |

## SecondaryMarketAgentsParams



| Field | Type | Description |
|-------|------|-------------|
| base_agent_dollars | Int |  |
| base_agent_sale_percentage | Float |  |
| sum_dollars_other_agents | Int |  |

## SecondaryMarket



| Field | Type | Description |
|-------|------|-------------|
| agents | SecondaryMarketAgents! |  |
| agents_params | SecondaryMarketAgentsParams |  |

## ProjectInfoDexSettings



| Field | Type | Description |
|-------|------|-------------|
| reserve | Int |  |
| tokens | Int |  |
| listing_price | Float |  |

## ProjectInfoCexSettings



| Field | Type | Description |
|-------|------|-------------|
| market_maker_dollars | Int |  |
| market_maker_tokens | Int |  |
| listing_price | Float |  |

## ProjectInfo



| Field | Type | Description |
|-------|------|-------------|
| dex | Boolean! |  |
| dex_settings | ProjectInfoDexSettings |  |
| cex | Boolean! |  |
| cex_settings | ProjectInfoCexSettings |  |

## Config



| Field | Type | Description |
|-------|------|-------------|
| name | String! |  |
| info | ProjectInfo! |  |
| primary_market | PrimaryMarket! |  |
| secondary_market | SecondaryMarket! |  |

## RunningSimulation



| Field | Type | Description |
|-------|------|-------------|
| id | String |  |
| project_name | String |  |
| project_symbol | String |  |
| agents | \[String] |  |
| agents_params | AgentsParams |  |
| liquidity_reserve | String |  |
| liquidity_tokens | String |  |
| createdAt | Int |  |

## FinishedSimulation



| Field | Type | Description |
|-------|------|-------------|
| id | String |  |
| project_name | String |  |
| project_symbol | String |  |
| execution_time_seconds | Int |  |
| agents | \[String] |  |
| agents_params | AgentsParams |  |
| liquidity_reserve | String |  |
| liquidity_tokens | String |  |
| score | Float |  |
| logo | String |  |
| slug | String! |  |
| scoring | ScoringData |  |
| createdAt | Int |  |

## GlobalStatistics



| Field | Type | Description |
|-------|------|-------------|
| project_count | Int |  |
| simulation_count | Int |  |
| total_execution_time_seconds | Int |  |
| total_simulation_data_in_kilobytes | Int |  |
| total_simulation_data_in_gigabytes | Float |  |

## ScorePoint



| Field | Type | Description |
|-------|------|-------------|
| score | Int |  |
| count | Int |  |

## Account



| Field | Type | Description |
|-------|------|-------------|
| address | ID! |  |

## ID

The `ID` scalar type represents a unique identifier, often used to refetch an object or as key for a cache. The ID type appears in a JSON response as a String; however, it is not intended to be human-readable. When expected as an input type, any string (such as `"4"`) or integer (such as `4`) input value will be accepted as an ID.


## AuthResponse



| Field | Type | Description |
|-------|------|-------------|
| token | String! |  |
| account | Account! |  |

## AccountAgentsParams



| Field | Type | Description |
|-------|------|-------------|
| base_agent_dollars | Int |  |
| base_agent_sale_percentage | Float |  |
| sum_dollars_other_agents | Int |  |

## AccountScoringData



| Field | Type | Description |
|-------|------|-------------|
| main_score | Float |  |
| average_score | \[Int] |  |
| categories | \[String] |  |

## AccountSimulation



| Field | Type | Description |
|-------|------|-------------|
| id | String |  |
| project_name | String |  |
| project_symbol | String |  |
| execution_time_seconds | Int |  |
| agents | \[String] |  |
| agents_params | AccountAgentsParams |  |
| liquidity_reserve | String |  |
| liquidity_tokens | String |  |
| score | Float |  |
| logo | String |  |
| slug | String! |  |
| scoring | AccountScoringData |  |
| createdAt | Int |  |

## GetAccountSimulationsOutput



| Field | Type | Description |
|-------|------|-------------|
| simulations | \[AccountSimulation] |  |
| nextToken | String |  |

## GetSimulationFromPromptOutput



| Field | Type | Description |
|-------|------|-------------|
| id | String! |  |
| slug | String! |  |

## Query



| Field | Type | Description |
|-------|------|-------------|
| authChallengeMessage | String | Request new challenge message. Used for login through "authLogin" in the next step. |
| authLogin | AuthResponse | Request temporary JWT token for login. |
| getAccountProfile | Account | Get your profile. Requires a valid token. |
| getAccountSimulations | GetAccountSimulationsOutput | Get your simulations. Requires a valid token. |
| getProject | Project | Get a single Project, based on it's slug. |
| getProjects | GetProjectsOutput | Get paginated list of Projects. |
| getSimulation | Simulation | Get single simulation. Requires Project slug and Simulation id. |
| getSimulations | GetSimulationsOutput | Get paginated list of Simulations for Project. Requires Project slug. |
| getLastConfig | Config | Get last used Simulation config for given Project. |
| getRunningSimulations | \[RunningSimulation] | Get paginated list of currently running Simulations. |
| getLastFinishedSimulations | \[FinishedSimulation] | Get last 10 finished Simulations. |
| getGlobalStatistics | GlobalStatistics | Get global statistics. |
| getGlobalSimulationScoreDistribution | \[ScorePoint] | Get Simulation score distribution across platform. |
| getGlobalProjectScoreDistribution | \[ScorePoint] | Get Project score distribution across platform. |

## Mutation



| Field | Type | Description |
|-------|------|-------------|
| createSimulation | String | Create new Simulation based on config parameters. |
| createSimulationFromPrompt | GetSimulationFromPromptOutput | Create new Simulation from given prompt. |

