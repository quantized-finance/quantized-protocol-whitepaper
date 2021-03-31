# quantized-protocol-whitepaper
The whitepaper for the Quantized protocol

The recent meteoric growth of bitcoin, ethereum and decentralized finance have proven to the world the value of the systems and shown that they are here to stay. Ethereum and the erc20 token are foundational to this new economy, and the erc20 token and ethereum evm have enabled a variety of applications never before possible in the world of finance. However, ethereum and the ERC 20 spec come with some significant drawbacks which make the economic activity on its Network less economical then it could be. 

Many solutions have been proposed to this problem, including things like layer 2 solutions and multi-blockchain networks. While each of these solutions has its advantage and utility, there are ways to gain significant efficiencies, and therefore cost savings, by employing ethereum protocols which are much more economical in how they transfer funds between addresses. 

The most advanced among these protocols is the ERC 1155 protocol, which is a multi-token protocol designed and implemented in such a way as to efficiently transfer values between internal endpoints with very low gas costs. Erc1155 enables transfers of multiple token types to multiple destinations in a single transaction in a highly efficient way.

The problem with these protocols is that the industry has widely adopted the use of erc20 tokens as the standard for fungible tokens, and thus it is largely impossible to move away to a new protocol which does a better job of transferring assets.

This whitepaper describes a protocol which functions to bring all of the efficiencies from ethereum's most advanced token transfer protocols to the existing defi environment, enhancing it by creating an enhanced 'quantized ERC20 specification' that features multi token transfer apis and dynamically deploys erc20 contracts backed by an ERC1155 implementation.

The protocol then incentivizes users to participate by rewarding them economically for converting their existing ERC 20 token into the quantized ERC version, and provides a standard means for determining the quantized erc20 token address for any existing erc20 token, while functioning as both an active liquidity provider for uniswap v2 and an additional source of liquidity as well. Paired with uniswap, quantized has the overall effect of driving the market towards lower fees and enabling more complex swaps that are economically viable without making any major infrastructural technological changes to existing defi infrastructure - Quantized ERC20 tokens function just like regular ERC20 tokens when transacted, except with lower fee, while offering very low fee multiparty transfers calls which substantially reduce gas fees in those appplications.

Quantized is a set of smart contracts which work to reduce the gas transfer fees of any ERC20 contract that employs it. Quantized does this by introducing a new set of transfer methods on quantized erc20 tokens which allow for multi-party transfers which are orders of magnitude less expensive than those performed now. 

Quantized achieves this by leveraging the ERC-1155 spec, mapping every ERC20 token to a single ERC 1155 contract, using create2 to deploy erc20 proxy contracts which map the erc20 contract interface with an equivalent ID on the erc1155 contract. These 'Quantized'Erc20 contracts when called employ the backing ERC 1155 contract implementation instead, enabling all ERC 1155-specific transfer functionality to be difrectly available to the ERC20 token, thus enabling the quantized ERC-20 to be transacted much more efficiently. 

In order to employ Quantized, a user is required to 'quantize' their erC 20 token. This process works by transferring the users erc20 tokens to the primary quantized contract and then minting an equivalent sum of quantized tokens of that type to the user. These quantized erc20 tokens are then equivalent to the original ERC 20 tokens held in custody, and can be redeemed at any time via an operation called dequantizing, which effectively reverses the process by returning the ERC 20 tokens to the user and burning the ERC 1155 quantized equivalent.

Quantized incentivizes participation by enforcing a fee to quantized tokens. However, this fee is not entirely kept by the quantized contract. Instead, the ERC 20 fee portion is kept,  but the user receives fee portion they paid back in Quanta, the native token of the quantized ecosystem. The fee for quantizing any ERC 20 token is currently 0.1%. however, this fee is controllable per erc20 address, and will be managed by Quantized governance.

Users are further incentivized to participate by receiving a initial quantization bonus. If the user is the first to quantize that ERC 20 token, the quantized system will use create2 to deploy an erc20 contract to enable users to transact in that new quantized token. This operation is gas-intensive. Users are incentivized to perform it by receiving a quanta bonus equivalent to 5% of the value of their rc20.

Quanta itself is pegged to ethereum, at a rate of 1 million quanta per ethereum. This effectively links the economic health of quanta to the economic health of the larger defi environment, encouraging early adopters to participate based on the anticipation of overall market growth.

Ethereum itself can be directly quantized, which has the effect of minting an equivalent portion of quanta back to the user at the fixed rate of 1 million quanta per ethereum. The ethereum received from the sale is held in custody by the quantized contract, and are allowed to purchase quanta up to the point where the quantized contract contains ethereum valued equivalently to the market value of all other ERC 20 contracts held in custody.

Users are disincentivized from exiting the system via being required to pay for that exit through either quanta or its current market value in ethereum. If the entire ecosystem is increasing in overall value, the quanta token will continue to increase in value. Exiting the system would mean either burning quanta they received when they entered which are now worth more than previously, or paying market rates for buying quanta in its uniswap pool. 

Quantized leverages create2 to predetermine the addresses of quantized erc20 tokens. This enables the creation of a quantized address for all ERC 20 tokens whether or not that token has been quantized yet, allowing to determine a tokens quantized address without interacting with Quanta itself. 

Quantized thus becomes a large erc20 liquidity pool, with internal funds available to be withdrawn, used and returned by anyone in the entire defi ecosystem just as with uniswap, acting as an optimizing force on the entire industry by incentivizing ERC 20 tokens that have real market value to perform the quantization process, receive the benefits of that optimization in a now - liquid token for doing so, then receiving further benefits as their transaction costs drop.

Unlike uniswalt owever, the creation of this liquidity pool is achieved as a function of the quantizing process, while still allowing the user the ability to transact the quantized derivative of the input tokens with no restriction, while either keeping the quanta token and receiving the system-wide optimization improvements gained as value assigned assigned by the market to quanta, whlle being free to exit the system should they wish. 

Whether or not the user chooses to permanently retain the quantized version of their token or not, the quantized environment is immediately and permanently benefited as soon as the users enters the system, because their initial fee portion in ERC20 is kept within the quantized contract permanently..


Quantized requires ERC 20 tokens that are quantized with it to have some known market value pegged to ethereum, and also requires that a source of market - priced  quanta liquidity be available to it for purchase when users choose to dequantize their tokens and pay for that fee in quanta. Both of these conditions are satisfied by requiring that every ERC 20 token  have a pre-existing uniswap liquidity pool before they can be quantized, and that a liquidity pool of quanta/ethereum exist for the quantized contract to employ. 

Quantized satisfies the first requirement by preventing ERC 20 contracts that do not have a uniswap liquidity pool from being quantized, and by incentivizing users to add liquidity to the unewap liquidity pool by allowing the user to sell the lp tokens directly to the quantized contract and receive quanta at a rate of 150% of the market value of their LP tokens (that value being calculated as the total value of the user's deposited quanta and ethereum)

Quantized then ensures that the funds within this liquidity pool are permanent by burning the lp tokens used to make the quanta purchase, locking that liquidity in the uniswap pool forever. 


Quantized is then able to both act as a source of liquidity like uniswap is, as well as an active liquidity provider to uniswap, providing uniswap with erc20 tokens and ethereum and receiving market maker fees from that activity, redepositing earned fees into the quantized contract, thus increasing the environments overall value. 


Beyond this immediate application, the concepts, code and models used and applied on quantized can be further extended to allow for the input of items which do not have a fungible quantity, such as nfts, while still outputting a fractionalized quantized product based on the market value of the nft has determined by other market sources. 

This allows for the intake of nonfungible items that have a known market value, such as uniswap v3 LP tokens, and immediately converting them into a number of fungible quantized , the size of which is predetermined when that nft is first quantized, minted to match the total market value of that nft, giving nfts quantized addresses just like erc20 tokens receive, and enabling them to be fractionalized using a standardized value metric received from the overall environment and via the activity of market participants on uniswap and the quantized platform.

Governance is implemented using a ticket-based governance system. Tickets are system change proposals that enable anyone to affect governance. Users pay to create a governance ticket that tightly describes the system update to be made. That ticket then is subject to a voting. Where governance token holders can vote on that ticket. If the majority votes to pass the ticket, then the ticket makes the changes to the Quantized contract setting. 

(Governance token distribution mechanism}. A portion of governance tokens is minted initially upon contract deployment and held by the quantized organization. The remainder of hovernance tokens are sold off directly to the public by the quantized contract, using a pricing mechanism that prices the tokens at an initial conversion rate then use the market maker algorithm to increase the price of the governance tokens until they are all sold off.. 
