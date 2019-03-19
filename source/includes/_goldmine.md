# goldmine

## Get Status

```shell
curl -i https://goldmine.provide.services/status
HTTP/2 204
```

This endpoint checks the status of the goldmine microservice.

#### HTTP Request

`GET /status`

## Networks
### Get Networks

```shell
curl -i \
    -H 'Authorization: bearer yoUr-AutH-TOKeN-FrOm-sIgnINg-in' \
    https://goldmine.provide.services/api/v1/networks
HTTP/2 200
```

> The above command returns JSON structured like this:

```json
{
        "id": "e5e0a051-6af7-4d1e-88cd-0ea1f67abd50",
        "created_at": "2018-10-10T14:56:11.812732Z",
        "application_id": null,
        "user_id": "3d9d62e8-0acf-47cd-b74f-52c1f96f8397",
        "name": "provide.network \"unicorn\" testnet CLONE",
        "description": null,
        "is_production": false,
        "cloneable": false,
        "enabled": true,
        "chain_id": "0x5bbe130b",
        "sidechain_id": null,
        "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
        "config": {
            "block_explorer_url": null,
            "chain": null,
            "chainspec": {
                "accounts": {
                    "0x0000000000000000000000000000000000000001": {
                        "balance": "1",
                        "builtin": {
                            "name": "ecrecover",
                            "pricing": {
                                "linear": {
                                    "base": 3000,
                                    "word": 0
                                }
                            }
                        }
                    },
                    ...
                    "0x0000000000000000000000000000000000000008": {
                        "balance": "1",
                        "builtin": {
                            "activate_at": "0x0",
                            "name": "alt_bn128_pairing",
                            "pricing": {
                                "alt_bn128_pairing": {
                                    "base": 100000,
                                    "pair": 80000
                                }
                            }
                        }
                    },
                    "0x0000000000000000000000000000000000000009": {
                        "balance": "1",
                        "constructor": "0x608060405234801561001057600080fd5b50611bfe806100206000..."
                    },
                    "0x0000000000000000000000000000000000000010": {
                        "balance": "1",
                        "constructor": "0x612988610030600b82828239805160001a60731460008114610020..."
                    },
                    "0x0000000000000000000000000000000000000011": {
                        "balance": "1",
                        "constructor": "0x610876610030600b82828239805160001a60731460008114610020..."
                    },
                    "0x0000000000000000000000000000000000000012": {
                        "balance": "1",
                        "constructor": "0x610f03610030600b82828239805160001a60731460008114610020..."
                    },
                    "0x0000000000000000000000000000000000000013": {
                        "balance": "1",
                        "constructor": "0x6110cc610030600b82828239805160001a60731460008114610020..."
                    },
                    "0x0000000000000000000000000000000000000014": {
                        "balance": "1",
                        "constructor": "0x610d6b610030600b82828239805160001a60731460008114610020..."
                    },
                    "0x0000000000000000000000000000000000000015": {
                        "balance": "1",
                        "constructor": "0x61032a610030600b82828239805160001a60731460008114610020..."
                    },
                    "0x0000000000000000000000000000000000000016": {
                        "balance": "1",
                        "constructor": "0x6101db610030600b82828239805160001a60731460008114610020..."
                    },
                    "0x0000000000000000000000000000000000000017": {
                        "balance": "1",
                        "constructor": "0x60806040523480156200001157600080fd5b506040516101208062..."
                    },
                    "0x9077F27fDD606c41822f711231eEDA88317aa67a": {
                        "balance": "1"
                    }
                },
                "engine": {
                    "authorityRound": {
                        "params": {
                            "blockReward": "0xDE0B6B3A7640000",
                            "maximumUncleCount": 0,
                            "maximumUncleCountTransition": 0,
                            "stepDuration": 5,
                            "validators": {
                                "multi": {
                                    "0": {
                                        "contract": "0x0000000000000000000000000000000000000017"
                                    }
                                }
                            }
                        }
                    }
                },
                "genesis": {
                    "difficulty": "0x20000",
                    "gasLimit": "0x7A1200",
                    "seal": {
                        "authorityRound": {
                            "signature": "0x000000000000000000000000000000000000...",
                            "step": "0x0"
                        }
                    }
                },
                "name": "unicorn",
                "params": {
                    "chainID": "0x5bbe130b",
                    "eip140Transition": "0x0",
                    "eip211Transition": "0x0",
                    "eip214Transition": "0x0",
                    "eip658Transition": "0x0",
                    "gasLimitBoundDivisor": "0x400",
                    "maximumExtraDataSize": "0x20",
                    "minGasLimit": "0x1388",
                    "networkID": "0x5bbe130b"
                },
                "subprotocolName": "prvd"
            },
            "chainspec_abi": {
                "0x0000000000000000000000000000000000000017": [
                    {
                        "constant": true,
                        "inputs": [
                            {
                                "name": "_validator",
                                "type": "address"
                            }
                        ],
                        "name": "getValidatorSupportCount",
                        "outputs": [
                            {
                                "name": "",
                                "type": "uint256"
                            }
                        ],
                        "payable": false,
                        "stateMutability": "view",
                        "type": "function"
                    },
                    ...
                    {
                        "constant": false,
                        "inputs": [
                            {
                                "name": "_validator",
                                "type": "address"
                            }
                        ],
                        "name": "removeValidator",
                        "outputs": null,
                        "payable": false,
                        "stateMutability": "nonpayable",
                        "type": "function"
                    },
                    {
                        "constant": false,
                        "inputs": [
                            {
                                "name": "_app_name",
                                "type": "bytes32"
                            },
                            {
                                "name": "_version_name",
                                "type": "bytes32"
                            },
                            {
                                "name": "_init",
                                "type": "address"
                            },
                            {
                                "name": "_init_sel",
                                "type": "bytes4"
                            },
                            {
                                "name": "_init_calldata",
                                "type": "bytes"
                            },
                            {
                                "name": "_fn_sels",
                                "type": "bytes4[]"
                            },
                            {
                                "name": "_fn_addrs",
                                "type": "address[]"
                            },
                            {
                                "name": "_version_desc",
                                "type": "bytes"
                            },
                            {
                                "name": "_init_desc",
                                "type": "bytes"
                            }
                        ],
                        "name": "deployConsensus",
                        "outputs": null,
                        "payable": false,
                        "stateMutability": "nonpayable",
                        "type": "function"
                    },
                    ...
                    {
                        "anonymous": false,
                        "inputs": [
                            {
                                "indexed": true,
                                "name": "supporter",
                                "type": "address"
                            },
                            {
                                "indexed": true,
                                "name": "supported",
                                "type": "address"
                            },
                            {
                                "indexed": true,
                                "name": "added",
                                "type": "bool"
                            }
                        ],
                        "name": "Support",
                        "type": "event"
                    }
                ]
            },
            "chainspec_abi_url": null,
            "chainspec_url": null,
            "cloneable_cfg": {
                "_security": {
                    "egress": "*",
                    "ingress": {
                        "0.0.0.0/0": {
                            "tcp": [
                                8050,
                                8051,
                                30300
                            ],
                            "udp": [
                                30300
                            ]
                        }
                    }
                },
                "aws": {
                    "docker": {
                        "regions": {
                            "ap-northeast-1": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            ...
                            "us-west-2": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            }
                        }
                    },
                    "ubuntu-vm": {
                        "regions": {
                            "ap-northeast-1": {
                                "peer": {
                                    "0.0.9": "ami-1e22e061"
                                },
                                "validator": {
                                    "0.0.9": "ami-1e22e061"
                                }
                            },
                            ...
                            "us-west-2": {
                                "peer": {
                                    "0.0.9": "ami-813777f9"
                                },
                                "validator": {
                                    "0.0.9": "ami-813777f9"
                                }
                            }
                        }
                    }
                }
            },
            "engine_id": "authorityRound",
            "is_ethereum_network": true,
            "is_load_balanced": false,
            "json_rpc_url": null,
            "native_currency": "PRVDDOC",
            "network_id": 1539183371,
            "parity_json_rpc_url": null,
            "protocol_id": "poa",
            "websocket_url": null
        },
        "stats": null
    }
```

This endpoint enumerates available blockchain Networks and related configuration details.

#### HTTP Request

`GET /api/v1/networks`

### Get a Specific Network

```shell
curl -i \
    -H 'Authorization: bearer yoUr-AutH-TOKeN-FrOm-sIgnINg-in' \
    https://goldmine.provide.services/api/v1/networks/e5e0a051-6af7-4d1e-88cd-0ea1f67abd50
HTTP/2 200
```

> The above command returns JSON structured like this:

```json
{
    "id": "e5e0a051-6af7-4d1e-88cd-0ea1f67abd50",
    "created_at": "2018-10-10T14:56:11.812732Z",
    "application_id": null,
    "user_id": "3d9d62e8-0acf-47cd-b74f-52c1f96f8397",
    "name": "provide.network \"unicorn\" testnet CLONE",
    "description": null,
    "is_production": false,
    "cloneable": false,
    "enabled": true,
    "chain_id": "0x5bbe130b",
    "sidechain_id": null,
    "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
    "config": {
        "block_explorer_url": null,
        "chain": null,
        "chainspec": {
            "accounts": {
                "0x0000000000000000000000000000000000000001": {
                    "balance": "1",
                    "builtin": {
                        "name": "ecrecover",
                        "pricing": {
                            "linear": {
                                "base": 3000,
                                "word": 0
                            }
                        }
                    }
                },
                ...
                "0x0000000000000000000000000000000000000008": {
                    "balance": "1",
                    "builtin": {
                        "activate_at": "0x0",
                        "name": "alt_bn128_pairing",
                        "pricing": {
                            "alt_bn128_pairing": {
                                "base": 100000,
                                "pair": 80000
                            }
                        }
                    }
                },
                "0x0000000000000000000000000000000000000009": {
                    "balance": "1",
                    "constructor": "0x608060405234801561001057600080fd5b50611bfe806100206000396..."
                },
                ...
                "0x0000000000000000000000000000000000000017": {
                    "balance": "1",
                    "constructor": "0x60806040523480156200001157600080fd5b50604051610120806200a..."
                },
                "0x9077F27fDD606c41822f711231eEDA88317aa67a": {
                    "balance": "1"
                }
            },
            "engine": {
                "authorityRound": {
                    "params": {
                        "blockReward": "0xDE0B6B3A7640000",
                        "maximumUncleCount": 0,
                        "maximumUncleCountTransition": 0,
                        "stepDuration": 5,
                        "validators": {
                            "multi": {
                                "0": {
                                    "contract": "0x0000000000000000000000000000000000000017"
                                }
                            }
                        }
                    }
                }
            },
            "genesis": {
                "difficulty": "0x20000",
                "gasLimit": "0x7A1200",
                "seal": {
                    "authorityRound": {
                        "signature": "0x0000000000000000000000000000000000000000000000000000000....",
                        "step": "0x0"
                    }
                }
            },
            "name": "unicorn",
            "params": {
                "chainID": "0x5bbe130b",
                "eip140Transition": "0x0",
                "eip211Transition": "0x0",
                "eip214Transition": "0x0",
                "eip658Transition": "0x0",
                "gasLimitBoundDivisor": "0x400",
                "maximumExtraDataSize": "0x20",
                "minGasLimit": "0x1388",
                "networkID": "0x5bbe130b"
            },
            "subprotocolName": "prvd"
        },
        "chainspec_abi": {
            "0x0000000000000000000000000000000000000017": [
                {
                    "constant": true,
                    "inputs": [
                        {
                            "name": "_validator",
                            "type": "address"
                        }
                    ],
                    "name": "getValidatorSupportCount",
                    "outputs": [
                        {
                            "name": "",
                            "type": "uint256"
                        }
                    ],
                    "payable": false,
                    "stateMutability": "view",
                    "type": "function"
                },
                ...
                {
                    "anonymous": false,
                    "inputs": [
                        {
                            "indexed": true,
                            "name": "supporter",
                            "type": "address"
                        },
                        {
                            "indexed": true,
                            "name": "supported",
                            "type": "address"
                        },
                        {
                            "indexed": true,
                            "name": "added",
                            "type": "bool"
                        }
                    ],
                    "name": "Support",
                    "type": "event"
                }
            ]
        },
        "chainspec_abi_url": null,
        "chainspec_url": null,
        "cloneable_cfg": {
            "_security": {
                "egress": "*",
                "ingress": {
                    "0.0.0.0/0": {
                        "tcp": [
                            8050,
                            8051,
                            30300
                        ],
                        "udp": [
                            30300
                        ]
                    }
                }
            },
            "aws": {
                "docker": {
                    "regions": {
                        "ap-northeast-1": {
                            "peer": "providenetwork-node",
                            "validator": "providenetwork-node"
                        },
                        ...
                        "us-west-2": {
                            "peer": "providenetwork-node",
                            "validator": "providenetwork-node"
                        }
                    }
                },
                "ubuntu-vm": {
                    "regions": {
                        "ap-northeast-1": {
                            "peer": {
                                "0.0.9": "ami-1e22e061"
                            },
                            "validator": {
                                "0.0.9": "ami-1e22e061"
                            }
                        },
                        ...
                        "us-west-2": {
                            "peer": {
                                "0.0.9": "ami-813777f9"
                            },
                            "validator": {
                                "0.0.9": "ami-813777f9"
                            }
                        }
                    }
                }
            }
        },
        "engine_id": "authorityRound",
        "is_ethereum_network": true,
        "is_load_balanced": false,
        "json_rpc_url": null,
        "native_currency": "PRVDDOC",
        "network_id": 1539183371,
        "parity_json_rpc_url": null,
        "protocol_id": "poa",
        "websocket_url": null
    },
    "stats": null
}
```

This endpoint retrieves details for the given Network.


#### HTTP Request

`GET /api/v1/networks/:id`

#### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the specific network


### Network Addresses

```shell
curl -i \
    -H 'Authorization: bearer yoUr-AutH-TOKeN-FrOm-sIgnINg-in' \
    https://goldmine.provide.services/api/v1/networks/e5e0a051-6af7-4d1e-88cd-0ea1f67abd50/addresses
HTTP/2 501
```

> The above command returns JSON structured like this:

```json
{
    "message": "not implemented"
}
```

This endpoint enumerates the addresses of the given Network.

<i> (Not yet implemented)</i>

#### HTTP Request

`GET /api/v1/networks/:id/addresses`

#### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the specific network

### Get Network Blocks

```shell
curl -i \
    -H 'Authorization: bearer yoUr-AutH-TOKeN-FrOm-sIgnINg-in' \
    https://goldmine.provide.services/api/v1/networks/e5e0a051-6af7-4d1e-88cd-0ea1f67abd50/blocks
HTTP/2 501
```

> The above command returns JSON structured like this:

```json
{
    "message": "not implemented"
}
```

This endpoint enumerates the blocks of the given Network.

<i> (Not yet implemented)</i>

#### HTTP Request

`GET /api/v1/networks/:id/blocks`

#### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the specific network

### Get Network contracts

```shell
curl -i \
    -H 'Authorization: bearer yoUr-AutH-TOKeN-FrOm-sIgnINg-in' \
    https://goldmine.provide.services/api/v1/networks/e5e0a051-6af7-4d1e-88cd-0ea1f67abd50/contracts
HTTP/2 200
```

> The above command returns JSON structured like this:

```json
{
        "id": "752eadfa-f138-4c73-a9b9-822a5bfb4dc6",
        "created_at": "0001-01-01T00:00:00Z",
        "application_id": null,
        "network_id": "e5e0a051-6af7-4d1e-88cd-0ea1f67abd50",
        "contract_id": null,
        "transaction_id": null,
        "name": "Network Contract 0x0000000000000000000000000000000000000017",
        "address": "0x0000000000000000000000000000000000000017",
        "params": null,
        "accessed_at": null
    }
```

This endpoint enumerates the contracts of the given Network.

#### HTTP Request

`GET /api/v1/networks/:id/contracts`

#### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the specific network

### Get Network transactions

```shell
curl -i \
    -H 'Authorization: bearer yoUr-AutH-TOKeN-FrOm-sIgnINg-in' \
    https://goldmine.provide.services/api/v1/networks/024ff1ef-7369-4dee-969c-1918c6edb5d4/transactions
HTTP/2 200
```

> The above command returns JSON structured like this:

```json
{
        "id": "f1125746-fa73-4392-a935-7a57faf3f7b0",
        "created_at": "2018-10-01T11:28:26.24501Z",
        "application_id": null,
        "user_id": "7062d7f8-d536-4c53-bba5-7486a8724ac3",
        "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
        "wallet_id": "f924d014-9d76-444a-b8e1-810bd3a75319",
        "to": null,
        "value": 0,
        "data": "0x6080604052604051602080612faa833981016040818152915160008054600160a060020a0383...",
        "hash": "0x79b9bef674435c69b25f7564c2cf216b2a3640343bce2a36067016f6a3811894",
        "status": "success",
        "params": null,
        "traces": null,
        "ref": null,
        "description": null
    },
    ...
    {
        "id": "44ce12a0-3779-4e0d-b095-ca15fec0a872",
        "created_at": "2018-09-01T05:55:22.7759Z",
        "application_id": null,
        "user_id": null,
        "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
        "wallet_id": "dfc12196-44d8-4ca2-8e6e-46f3ccf4c3a8",
        "to": "0x139c328F1fF7910757E63F5045469CbDE18152b2",
        "value": 0,
        "data": "0x676f7fec31313233343500000000000000000000000000000000000000000000000000003031...",
        "hash": "0x8584a8a2167868c3dbd948e3eade46ae0c98ca43bdf7d7e17b0693fabf004690",
        "status": "success",
        "params": null,
        "traces": null,
        "ref": "bd90e2e8-60a4-4522-89ce-53fe0611b268",
        "description": null
    }
```

This endpoint enumerates the transactions of the given Network.


#### HTTP Request

`GET /api/v1/networks/:id/transactions`

#### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the specific network

### Get Network transaction details

```shell
curl -i \
    -H 'Authorization: bearer yoUr-AutH-TOKeN-FrOm-sIgnINg-in' \
    https://goldmine.provide.services/api/v1/networks/024ff1ef-7369-4dee-969c-1918c6edb5d4/transactions/f1125746-fa73-4392-a935-7a57faf3f7b0
HTTP/2 200
```

> The above command returns JSON structured like this:

```json
{
    "id": "f1125746-fa73-4392-a935-7a57faf3f7b0",
    "created_at": "2018-10-01T11:28:26.24501Z",
    "application_id": null,
    "user_id": "7062d7f8-d536-4c53-bba5-7486a8724ac3",
    "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
    "wallet_id": "f924d014-9d76-444a-b8e1-810bd3a75319",
    "to": null,
    "value": 0,
    "data": "0x6080604052604051602080612faa833981016040818152915160008054600160a060020a03831660...",
    "hash": "0x79b9bef674435c69b25f7564c2cf216b2a3640343bce2a36067016f6a3811894",
    "status": "success",
    "params": null,
    "traces": {
        "result": [
            {
                "action": {
                    "callType": null,
                    "from": "0x8cd7e456d1276e7074b10ae94dcd25f62d1ea147",
                    "gas": "0x2516fd",
                    "init": "0x6080604052604051602080612faa833981016040818152915160008054600160...",
                    "input": null,
                    "to": null,
                    "value": "0x0"
                },
                "blockHash": "0x519dd9d06775eb36d0795c469ed6892f12c5dadc881916f29cca3de9c4fd238d",
                "blockNumber": 2348545,
                "result": {
                    "address": "0x2e49f7d86daf4c3590646c4c2619b2956e8e027b",
                    "code": "0x608060405260043610620000955763ffffffff60e060020a6000350416632e9d...",
                    "gasUsed": "0x2516fd",
                    "output": null
                },
                "error": null,
                "subtraces": 0,
                "traceAddress": [],
                "transactionHash": "0x79b9bef674435c69b25f7564c2cf216b2a3640343bce2a36067016f6a3811894",
                "transactionPosition": 0,
                "type": "create"
            }
        ]
    },
    "ref": null,
    "description": null
}
```

This endpoint retrieves the details of the Network’s specified Transaction.


#### HTTP Request

`GET /api/v1/networks/:id/transactions/:transactionId`

#### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the specific network
transactionId | The ID of the specific transaction

### Update a Network

```shell
curl -i -XPUT \
    -H 'Authorization: bearer yoUr-AutH-TOKeN-FrOm-sIgnINg-in' \
    https://goldmine.provide.services/api/v1/networks/e5e0a051-6af7-4d1e-88cd-0ea1f67abd50 \
    -d '{"name": "provide.network \"unicorn\" testnet CLONE now with more update"}'
HTTP/2 204
```


This endpoint updates a given Network.


#### HTTP Request

`PUT /api/v1/networks/:id`

#### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the specific network

### Get a Network's Contract details

```shell
curl -i \
    -H 'Authorization: bearer yoUr-AutH-TOKeN-FrOm-sIgnINg-in' \
    https://goldmine.provide.services/api/v1/networks/e5e0a051-6af7-4d1e-88cd-0ea1f67abd50/contracts/752eadfa-f138-4c73-a9b9-822a5bfb4dc6
HTTP/2 200
```

> The above command returns JSON structured like this:

```json
{
    "id": "752eadfa-f138-4c73-a9b9-822a5bfb4dc6",
    "created_at": "2018-10-10T14:56:11.84238Z",
    "application_id": null,
    "network_id": "e5e0a051-6af7-4d1e-88cd-0ea1f67abd50",
    "contract_id": null,
    "transaction_id": null,
    "name": "Network Contract 0x0000000000000000000000000000000000000017",
    "address": "0x0000000000000000000000000000000000000017",
    "params": {
        "abi": [
            {
                "constant": true,
                "inputs": [
                    {
                        "name": "_validator",
                        "type": "address"
                    }
                ],
                "name": "getValidatorSupportCount",
                "outputs": [
                    {
                        "name": "",
                        "type": "uint256"
                    }
                ],
                "payable": false,
                "stateMutability": "view",
                "type": "function"
            },
            ...
            {
                "anonymous": false,
                "inputs": [
                    {
                        "indexed": true,
                        "name": "supporter",
                        "type": "address"
                    },
                    {
                        "indexed": true,
                        "name": "supported",
                        "type": "address"
                    },
                    {
                        "indexed": true,
                        "name": "added",
                        "type": "bool"
                    }
                ],
                "name": "Support",
                "type": "event"
            }
        ],
        "name": "Network Contract 0x0000000000000000000000000000000000000017"
    },
    "accessed_at": null
}
```

This endpoint retrieves the details of the Network's specified Contract.


#### HTTP Request

`GET /api/v1/networks/:id/contracts/:contractId`

#### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the specific network
contractId | The ID of the specified contract

### Create a new Network

```shell
curl -i \
    -H 'Authorization: bearer yoUr-AutH-TOKeN-FrOm-sIgnINg-in' \
    https://goldmine.provide.services/api/v1/networks \
    -d '{"config": {
            "block_explorer_url": null,
            "chain": null,
            "chainspec": {
              "accounts": {
                "0x0000000000000000000000000000000000000001": {
                  "balance": "1",
                  "builtin": {
                    "name": "ecrecover",
                    "pricing": {
                      "linear": {
                        "base": 3000,
                        "word": 0
                      }
                    }
                  }
                },
                "0x0000000000000000000000000000000000000008": {
                  "balance": "1",
                  "builtin": {
                    "activate_at": "0x0",
                    "name": "alt_bn128_pairing",
                    "pricing": {
                      "alt_bn128_pairing": {
                        "base": 100000,
                        "pair": 80000
                      }
                    }
                  }
                },
                "0x0000000000000000000000000000000000000009": {
                  "balance": "1",
                  "constructor": "0x608060405234801561001057600080fd5b50611a7f8061..."
                },
                "0x0000000000000000000000000000000000000010": {
                  "balance": "1",
                  "constructor": "0x6116ad610030600b82828239805160001a607314600081..."
                }
              },
              "engine": {
                "authorityRound": {
                  "params": {
                    "blockReward": "0xDE0B6B3A7640000",
                    "maximumUncleCount": 0,
                    "maximumUncleCountTransition": 0,
                    "stepDuration": 5,
                    "validators": {
                      "multi": {
                        "0": {
                          "contract": "0x0000000000000000000000000000000000000018"
                        }
                      }
                    }
                  }
                }
              },
              "genesis": {
                "difficulty": "0x20000",
                "gasLimit": "0x7A1200",
                "seal": {
                  "authorityRound": {
                    "signature": "0x0000000000000000000000000000000000000000000000...",
                    "step": "0x0"
                  }
                }
              },
              "name": "unicornv2",
              "params": {
                "chainID": "0x5ba25d96",
                "eip140Transition": "0x0",
                "eip211Transition": "0x0",
                "eip214Transition": "0x0",
                "eip658Transition": "0x0",
                "gasLimitBoundDivisor": "0x400",
                "maximumExtraDataSize": "0x20",
                "minGasLimit": "0x1388",
                "networkID": "0x5ba25d96"
              },
              "subprotocolName": "prvd"
            },
            "chainspec_abi": {
              "0x0000000000000000000000000000000000000010": [
                {
                  "constant": true,
                  "inputs": null,
                  "name": "init",
                  "outputs": null,
                  "payable": false,
                  "stateMutability": "view",
                  "type": "function"
                },
                {
                  "constant": true,
                  "inputs": [
                    {
                      "name": "_storage",
                      "type": "address"
                    },
                    {
                      "name": "_exec_id",
                      "type": "bytes32"
                    },
                    {
                      "name": "_provider",
                      "type": "address"
                    }
                  ],
                  "name": "getApplications",
                  "outputs": [
                    {
                      "name": "",
                      "type": "bytes32[]"
                    }
                  ],
                  "payable": false,
                  "stateMutability": "view",
                  "type": "function"
                }
              ]
            },
            "chainspec_abi_url": null,
            "chainspec_url": null,
            "cloneable_cfg": {
              "_security": {
                "egress": "*",
                "ingress": {
                  "0.0.0.0/0": {
                    "tcp": [
                      5001,
                      8050,
                      8051,
                      8080,
                      30300
                    ],
                    "udp": [
                      30300
                    ]
                  }
                }
              },
              "aws": {
                "docker": {
                  "regions": {
                    "ap-northeast-1": {
                      "peer": "providenetwork-node",
                      "validator": "providenetwork-node"
                    },
                    "ap-northeast-2": {
                      "peer": "providenetwork-node",
                      "validator": "providenetwork-node"
                    }
                  }
                },
                "ubuntu-vm": {
                  "regions": {
                    "ap-northeast-1": {
                      "peer": {
                        "0.0.9": "ami-1e22e061"
                      },
                      "validator": {
                        "0.0.9": "ami-1e22e061"
                      }
                    },
                    "ap-northeast-2": {
                      "peer": {
                        "0.0.9": "ami-bfa802d1"
                      },
                      "validator": {
                        "0.0.9": "ami-bfa802d1"
                      }
                    }
                  }
                }
              }
            },
            "engine_id": "authorityRound",
            "is_ethereum_network": true,
            "is_load_balanced": false,
            "json_rpc_url": null,
            "native_currency": "PRVD",
            "network_id": null,
            "parity_json_rpc_url": null,
            "protocol_id": "poa",
            "websocket_url": null
          },
          "name": "provide.network \"unicorn v2\" testnet clone",
          "network_id": "36a5f8e0-bfc1-49f8-a7ba-86457bb52912",
          "cloneable": false,
          "enabled": true,
          "is_production": false
        }'
HTTP/2 201
```

> The above command returns JSON structured like this:

```json
{
  "id": "4617eb8c-4f74-4262-b626-9616ab6fa413",
  "created_at": "2018-10-15T02:22:19.585422693Z",
  "application_id": null,
  "user_id": "7062d7f8-d536-4c53-bba5-7486a8724ac3",
  "name": "provide.network \"unicorn v2\" testnet clone",
  "description": null,
  "is_production": false,
  "cloneable": false,
  "enabled": true,
  "chain_id": "0x5bc3f9db",
  "sidechain_id": null,
  "network_id": "36a5f8e0-bfc1-49f8-a7ba-86457bb52912",
  "config": {
    "block_explorer_url": null,
    "chain": null,
    "chainspec": {
      "accounts": {
        "0x0000000000000000000000000000000000000001": {
          "balance": "1",
          "builtin": {
            "name": "ecrecover",
            "pricing": {
              "linear": {
                "base": 3000,
                "word": 0
              }
            }
          }
        },
        "0x0000000000000000000000000000000000000002": {
          "balance": "1",
          "builtin": {
            "name": "sha256",
            "pricing": {
              "linear": {
                "base": 60,
                "word": 12
              }
            }
          }
        }
      },
      "engine": {
        "authorityRound": {
          "params": {
            "blockReward": "0xDE0B6B3A7640000",
            "maximumUncleCount": 0,
            "maximumUncleCountTransition": 0,
            "stepDuration": 5,
            "validators": {
              "multi": {
                "0": {
                  "contract": "0x0000000000000000000000000000000000000018"
                }
              }
            }
          }
        }
      },
      "genesis": {
        "difficulty": "0x20000",
        "gasLimit": "0x7A1200",
        "seal": {
          "authorityRound": {
            "signature": "0x000000000000000000000000000000000000000000000000...",
            "step": "0x0"
          }
        }
      },
      "name": "unicornv2",
      "params": {
        "chainID": "0x5bc3f9db",
        "eip140Transition": "0x0",
        "eip211Transition": "0x0",
        "eip214Transition": "0x0",
        "eip658Transition": "0x0",
        "gasLimitBoundDivisor": "0x400",
        "maximumExtraDataSize": "0x20",
        "minGasLimit": "0x1388",
        "networkID": "0x5bc3f9db"
      },
      "subprotocolName": "prvd"
    },
    "chainspec_abi": {
      "0x0000000000000000000000000000000000000009": [
        {
          "anonymous": false,
          "inputs": [
            {
              "indexed": true,
              "name": "execution_id",
              "type": "bytes32"
            },
            {
              "indexed": true,
              "name": "index",
              "type": "address"
            },
            {
              "indexed": false,
              "name": "script_exec",
              "type": "address"
            }
          ],
          "name": "ApplicationInitialized",
          "type": "event"
        },
        {
          "anonymous": false,
          "inputs": [
            {
              "indexed": true,
              "name": "execution_id",
              "type": "bytes32"
            },
            {
              "indexed": true,
              "name": "script_target",
              "type": "address"
            }
          ],
          "name": "ApplicationExecution",
          "type": "event"
        }
      ],
      "0x0000000000000000000000000000000000000010": [
        {
          "constant": true,
          "inputs": null,
          "name": "init",
          "outputs": null,
          "payable": false,
          "stateMutability": "view",
          "type": "function"
        }
      ]
    },
    "chainspec_abi_url": null,
    "chainspec_url": null,
    "cloneable_cfg": {
      "_security": {
        "egress": "*",
        "ingress": {
          "0.0.0.0/0": {
            "tcp": [
              5001,
              8050,
              8051,
              8080,
              30300
            ],
            "udp": [
              30300
            ]
          }
        }
      },
      "aws": {
        "docker": {
          "regions": {
            "ap-northeast-1": {
              "peer": "providenetwork-node",
              "validator": "providenetwork-node"
            },
            "ap-northeast-2": {
              "peer": "providenetwork-node",
              "validator": "providenetwork-node"
            }
          }
        },
        "ubuntu-vm": {
          "regions": {
            "ap-northeast-1": {
              "peer": {
                "0.0.9": "ami-1e22e061"
              },
              "validator": {
                "0.0.9": "ami-1e22e061"
              }
            },
            "ap-northeast-2": {
              "peer": {
                "0.0.9": "ami-bfa802d1"
              },
              "validator": {
                "0.0.9": "ami-bfa802d1"
              }
            }
          }
        }
      }
    },
    "engine_id": "authorityRound",
    "is_ethereum_network": true,
    "is_load_balanced": false,
    "json_rpc_url": null,
    "native_currency": "PRVD",
    "network_id": 1539570139,
    "parity_json_rpc_url": null,
    "protocol_id": "poa",
    "websocket_url": null
  },
  "stats": null
}
```

This endpoint creates a new Network.


#### HTTP Request

`POST /api/v1/networks`


### Get a Network's Bridges

```shell
curl -i \
    -H 'Authorization: bearer yoUr-AutH-TOKeN-FrOm-sIgnINg-in' \
    https://goldmine.provide.services/api/v1/networks/e5e0a051-6af7-4d1e-88cd-0ea1f67abd50/bridges
HTTP/2 501
```

> The above command returns JSON structured like this:

```json
{
    "message": "not implemented"
}
```

This endpoint enumerates the specified Network’s Bridges.

<i> (Not yet implemented)</i>


#### HTTP Request

`GET /api/v1/networks/:id/bridges`

#### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the specific network

### Get a Network's Connectors

```shell
curl -i \
    -H 'Authorization: bearer yoUr-AutH-TOKeN-FrOm-sIgnINg-in' \
    https://goldmine.provide.services/api/v1/networks/e5e0a051-6af7-4d1e-88cd-0ea1f67abd50/connectors
HTTP/2 501
```

> The above command returns JSON structured like this:

```json
{
    "message": "not implemented"
}
```

This endpoint enumerates the specified Network’s Connectors.

<i> (Not yet implemented)</i>

#### HTTP Request

`GET /api/v1/networks/:id/connectors`

#### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the specific network

### Get a Network's Nodes

```shell
curl -i \
    -H 'Authorization: bearer yoUr-AutH-TOKeN-FrOm-sIgnINg-in' \
    https://goldmine.provide.services/api/v1/networks/024ff1ef-7369-4dee-969c-1918c6edb5d4/nodes
HTTP/2 200
```

> The above command returns JSON structured like this:

```json
{
    "id": "59d1e7ce-3316-45b2-bf06-5fae2c6294fe",
    "created_at": "2018-09-06T08:13:14.109926Z",
    "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
    "user_id": "7062d7f8-d536-4c53-bba5-7486a8724ac3",
    "is_bootnode": true,
    "host": "ec2-18-206-200-4.compute-1.amazonaws.com",
    "description": null,
    "role": "peer",
    "status": "running",
    "config": {
      "default_json_rpc_port": null,
      "default_websocket_port": null,
      "engine_id": "authorityRound",
      "env": {
        "BOOTNODES": "enode://eb0543bf6c960ad79...",
        "CHAIN": "unicorn-v0",
        "CHAIN_SPEC_URL": "https://console.provide.services:443/api/networks/024ff1ef-7369-4dee-969c-1918c6edb5d4/spec.json?x-api-authorization=MjE3Nzc4...",
        "ENGINE_SIGNER": "0xc8cf82765ccc99e5d878A245f7eC9ECe8F9Fae4d",
        "ENGINE_SIGNER_KEY_JSON": "{\"id\":\"120354c2-f2d5-...\"}",
        "ENGINE_SIGNER_PRIVATE_KEY": "b9dc0beec2d7f9...",
        "NETWORK_ID": "22",
        "PEER_SET": "required:eb0543bf6c960ad79a9..."
      },
      "peer_url": "enode://46cd112cbcc91cfe410a697...",
      "protocol_id": "poa",
      "provider_id": "docker",
      "region": "us-east-1",
      "role": "peer",
      "target_id": "aws",
      "target_security_group_ids": [
        "sg-0f29ec025b64c0a44"
      ],
      "target_task_ids": [
        "arn:aws:ecs:us-east-1:085843810865:task/58953fe..."
      ]
    }
  }
```

This endpoint enumerates the specified Network’s Nodes.


#### HTTP Request

`GET /api/v1/networks/:id/nodes`

#### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the specific network

### Create a new Network Node

```shell
curl -i \
    -H 'Authorization: bearer youR-ToKEn' \
    https://goldmine.provide.services/api/networks/4617eb8c-4f74-4262-b626-9616ab6fa413/nodes \
    -d '{
  "network_id": "4617eb8c-4f74-4262-b626-9616ab6fa413",
  "config": {
    "protocol_id": "poa",
    "engine_id": "authorityRound",
    "target_id": "aws",
    "provider_id": "docker",
    "role": "validator",
    "engines": "[{\"id\":\"authorityRound\",\"name\":\"Authority Round\",\"enabled\":true}]",
    "providers": "[{\"id\":\"ubuntu-vm\",\"name\":\"Ubuntu\",\"...\":\"...\"}]",
    "roles": "[{\"id\":\"peer\",\"name\":\"Peer\",\"config\":{\"...\":\"...\"]}]",
    "credentials": {
      "aws_access_key_id": "AKIA...",
      "aws_secret_access_key": "MtM/6RZw0..."
    },
    "env": {
      "CHAIN_SPEC_URL": "https://api.provide.services/api/networks/4617eb8c-4f74-4262-b626-9616ab6fa413/spec.json?x-api-authorization=eyJhbGci...",
      "CHAIN": "unicorn-v0",
      "ENGINE_SIGNER": "0x...",
      "NETWORK_ID": "1539570139"
    },
    "rc.d": "{\n  \"CHAIN_SPEC_URL\": \"https://api.provide.services/api/networks/4617eb8c-4f74-4262-b626-9616ab6fa413/spec.json?x-api-authorization=eyJhbGciOiJI...\",\n  \"CHAIN\": \"unicorn-v0\",\n  \"ENGINE_SIGNER\": \"0x...\",\n  \"NETWORK_ID\": \"1539570139\",\n  \"ENGINE_SIGNER_PRIVATE_KEY\": null\n}",
    "region": "us-east-1"
  }
}'
```

> The above command returns JSON structured like this:

```json
{
  "id": "4721cca3-fa2e-4085-b675-c5bea777c408",
  "created_at": "2018-10-15T02:42:10.375957413Z",
  "network_id": "4617eb8c-4f74-4262-b626-9616ab6fa413",
  "user_id": "7062d7f8-d536-4c53-bba5-7486a8724ac3",
  "is_bootnode": false,
  "host": null,
  "description": null,
  "role": "validator",
  "status": "pending",
  "config": {
    "protocol_id": "poa",
    "engine_id": "authorityRound",
    "target_id": "aws",
    "provider_id": "docker",
    "role": "validator",
    "engines": "[{\"id\":\"authorityRound\",\"name\":\"Authority Round\",\"enabled\":true}]",
    "providers": "[{\"id\":\"ubuntu-vm\",\"name\":\"Ubuntu\",\"img_src_dark\":\"...\"}]",
    "roles": "[{\"id\":\"peer\",\"name\":\"Peer\",\"config\":{...}]",
    "credentials": {
      "aws_access_key_id": "AKIAJ5Y...",
      "aws_secret_access_key": "MtM/6..."
    },
    "env": {
      "CHAIN_SPEC_URL": "https://api.provide.services/api/networks/4617eb8c-4f74-4262-b626-9616ab6fa413/spec.json?x-api-authorization=eyJhbGciOiJIUz...",
      "CHAIN": "unicorn-v0",
      "ENGINE_SIGNER": "0x16E8950...",
      "NETWORK_ID": "1539570139"
    },
    "rc.d": "{\n  \"CHAIN_SPEC_URL\": \"https://api.provide.services/api/networks/4617eb8c-4f74-4262-b626-9616ab6fa413/spec.json?x-api-authorization=eyJhbGci...\",\n  \"CHAIN\": \"unicorn-v0\",\n  \"ENGINE_SIGNER\": \"0x...\",\n  \"NETWORK_ID\": \"1539570139\",\n  \"ENGINE_SIGNER_PRIVATE_KEY\": null\n}",
    "region": "us-east-1"
  }
}
```

This endpoint creates a new Node on the given Network.


#### HTTP Request

`POST /api/v1/networks/:id/nodes`

#### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the specific network

### Get a specific Network Node

```shell
curl -i \
    -H 'Authorization: bearer an-apPliCaTIOn-aPi-tOkEn' \
    https://goldmine.provide.services/api/v1/networks/024ff1ef-7369-4dee-969c-1918c6edb5d4/nodes/59d1e7ce-3316-45b2-bf06-5fae2c6294fe
HTTP/2 200
```

> The above command returns JSON structured like this:

```json
{
    "id": "59d1e7ce-3316-45b2-bf06-5fae2c6294fe",
    "created_at": "2018-09-06T08:13:14.109926Z",
    "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
    "user_id": "7062d7f8-d536-4c53-bba5-7486a8724ac3",
    "is_bootnode": true,
    "host": "ec2-18-206-200-4.compute-1.amazonaws.com",
    "description": null,
    "role": "peer",
    "status": "running",
    "config": {
        "credentials": {
            "aws_access_key_id": "AKIAIF...",
            "aws_secret_access_key": "azrrYySnS..."
        },
        "default_json_rpc_port": null,
        "default_websocket_port": null,
        "engine_id": "authorityRound",
        "engines": [
            {
                "enabled": true,
                "id": "authorityRound",
                "name": "Authority Round"
            }
        ],
        "env": {
            "BOOTNODES": "enode://eb0543bf6c9...",
            "CHAIN": "unicorn-v0",
            "CHAIN_SPEC_URL": "https://console.provide.services:443/api/networks/024ff1ef-7369-4dee-969c-1918c6edb5d4/spec.json?x-api-authorization=MjE3N...",
            "ENGINE_SIGNER": "0xc8...",
            "ENGINE_SIGNER_KEY_JSON": "{\"id\":\"...\"}",
            "ENGINE_SIGNER_PRIVATE_KEY": "b9dc0...",
            "NETWORK_ID": "22",
            "PEER_SET": "required:eb0543bf6c960a..."
        },
        "peer_url": "enode://46cd112cbcc91cfe410...",
        "protocol_id": "poa",
        "provider_id": "docker",
        "providers": [
            {
                "enabled": true,
                "id": "ubuntu-vm",
                "img_src": "https://s3.amazonaws.com/provide.services/img/ubuntu.png",
                "name": "Ubuntu"
            },
            {
                "enabled": true,
                "id": "docker",
                "img_src": "https://s3.amazonaws.com/provide.services/img/docker.png",
                "name": "Docker"
            }
        ],
        "rc.d": "{\n  \"CHAIN_SPEC_URL\": \"https://console.provide.services:443/api/networks/024ff1ef-7369-4dee-969c-1918c6edb5d4/spec.json?x-api-authorization=MjE3Nzc...\",\n  \"BOOTNODES\": \"enode://eb0543bf6c9...\",\n  \"NETWORK_ID\": \"22\"\n}",
        "region": "us-east-1",
        "role": "peer",
        "roles": [
            {
                "config": {
                    "allows_multiple_deployment": true,
                    "default_rcd": {
                        "provide.network": "#!/bin/bash\n\nservice provide.network stop\n...\n"
                    },
                    "quickclone_recommended_node_count": 2
                },
                "id": "peer",
                "name": "Peer",
                "supported_provider_ids": [
                    "ubuntu-vm",
                    "docker"
                ]
            },
            {
                "config": {
                    "allows_multiple_deployment": false,
                    "default_rcd": {
                        "docker": {
                            "provide.network": "{\"CHAIN_SPEC_URL\": null, \"ENGINE_SIGNER\": null, \"NETWORK_ID\": null, \"ENGINE_SIGNER_PRIVATE_KEY\": null}"
                        },
                        "ubuntu-vm": {
                            "provide.network": "#!/bin/bash\n\nservice provide.network stop\n...\n"
                        }
                    },
                    "quickclone_recommended_node_count": 1
                },
                "id": "validator",
                "name": "Validator",
                "supported_provider_ids": [
                    "ubuntu-vm",
                    "docker"
                ]
            },
            {
                "config": {
                    "allows_multiple_deployment": false,
                    "default_rcd": {
                        "docker": {
                            "provide.network": "{\"JSON_RPC_URL\": null}"
                        }
                    },
                    "quickclone_recommended_node_count": 1
                },
                "id": "explorer",
                "name": "Block Explorer",
                "supported_provider_ids": [
                    "ubuntu-vm",
                    "docker"
                ]
            }
        ],
        "target_id": "aws",
        "target_security_group_ids": [
            "sg-0f29..."
        ],
        "target_task_ids": [
            "arn:aws:ecs:us-east-1:085843810865:task/58953..."
        ]
    }
}
```

This endpoint retrieves the details of the Network’s specified Node.


#### HTTP Request

`GET /api/v1/networks/:id/nodes/:nodeId`

#### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the specific network
nodeId | The ID of the specified Node

### Get logs for a specific Network Node

```shell
curl -i \
    -H 'Authorization: bearer an-apPliCaTIOn-aPi-tOkEn' \
    https://goldmine.provide.services/api/v1/networks/024ff1ef-7369-4dee-969c-1918c6edb5d4/nodes/59d1e7ce-3316-45b2-bf06-5fae2c6294fe/logs
HTTP/2 200
```

> The above command returns logs structured like this:

```[
    "2018-10-12 03:07:50 UTC Verifier #1 INFO import  Imported #2532534 0x4720…9c60 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 03:07:53 UTC IO Worker #1 INFO import          #0    3/25 peers      5 MiB chain   95 MiB db  0 bytes queue  573 KiB sync  RPC:  0 conn,    0 req/s,  179 µs",
    "2018-10-12 03:07:55 UTC Verifier #0 INFO import  Imported #2532535 0xb01b…3150 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 03:08:00 UTC Verifier #1 INFO import  Imported #2532536 0x64c7…b825 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 03:08:05 UTC Verifier #0 INFO import  Imported #2532537 0xccb4…d9da (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 03:08:10 UTC Verifier #1 INFO import  Imported #2532538 0x70ed…97ea (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 03:08:15 UTC Verifier #0 INFO import  Imported #2532539 0x75c5…1712 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 03:08:20 UTC Verifier #1 INFO import  Imported #2532540 0xbb17…a470 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 03:08:25 UTC Verifier #0 INFO import  Imported #2532541 0x61d8…37a8 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 03:08:28 UTC IO Worker #2 INFO import          #0    3/25 peers      5 MiB chain   95 MiB db  0 bytes queue  573 KiB sync  RPC:  0 conn,    0 req/s,  167 µs",
    ...
    "2018-10-12 11:42:30 UTC Verifier #0 INFO import  Imported #2538710 0x320b…da62 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 11:42:35 UTC Verifier #1 INFO import  Imported #2538711 0x00b2…3346 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 11:42:40 UTC Verifier #0 INFO import  Imported #2538712 0xdbba…9811 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 11:42:45 UTC Verifier #1 INFO import  Imported #2538713 0x473d…2c6c (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 11:42:50 UTC Verifier #0 INFO import  Imported #2538714 0x194a…fffb (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 11:42:55 UTC Verifier #1 INFO import  Imported #2538715 0xd854…cca5 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 11:43:00 UTC Verifier #0 INFO import  Imported #2538716 0x5249…1343 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 11:43:04 UTC IO Worker #1 INFO import          #0    3/25 peers      4 MiB chain   95 MiB db  0 bytes queue  573 KiB sync  RPC:  0 conn, 6558 req/s,  173 µs",
    "2018-10-12 11:43:05 UTC Verifier #1 INFO import  Imported #2538717 0xdf84…3b4d (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 11:43:10 UTC Verifier #1 INFO import  Imported #2538718 0x888d…7b65 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
]
```

This endpoint retrieves the logs for the specified Node.


#### HTTP Request

`GET /api/v1/networks/:id/nodes/:nodeId/logs`

#### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the specific network
nodeId | The ID of the specified Node

### Delete a Specific Node

```shell
curl -i -XDELETE \
    -H 'Authorization: bearer an-apPliCaTIOn-aPi-tOkEn' \
    https://goldmine.provide.services/api/v1/networks/024ff1ef-7369-4dee-969c-1918c6edb5d4/nodes/59d1e7ce-3316-45b2-bf06-5fae2c6294fe
HTTP/2 204
```


This endpoint removes the Network’s specified Node.


#### HTTP Request

`DELETE /api/v1/networks/:id/nodes/:nodeId`

#### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the specific network
nodeId | The ID of the specified Node

### Get a Network's Oracles

```shell
curl -i \
    -H 'Authorization: bearer yoUr-AutH-TOKeN-FrOm-sIgnINg-in' \
    https://goldmine.provide.services/api/v1/networks/e5e0a051-6af7-4d1e-88cd-0ea1f67abd50/oracles
```

> The above command returns JSON structured like this:

```json
{
    "message": "not implemented"
}
```

This endpoint enumerates the specified Network’s Oracles.

<i> (Not yet implemented) </i>


#### HTTP Request

`GET /api/v1/networks/:id/oracles`

#### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the specific network

### Get a Network's Tokens

```shell
curl -i \
    -H 'Authorization: bearer yoUr-AutH-TOKeN-FrOm-sIgnINg-in' \
    https://goldmine.provide.services/api/v1/networks/024ff1ef-7369-4dee-969c-1918c6edb5d4/tokens
HTTP/2 200
```


This endpoint enumerates the specified Network’s Tokens.


#### HTTP Request

`GET /api/v1/networks/:id/tokens`

#### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the specific network

### Get a Network's Status

```shell
curl -i \
    -H 'Authorization: bearer yoUr-AutH-TOKeN-FrOm-sIgnINg-in' \
    https://goldmine.provide.services/api/v1/networks/024ff1ef-7369-4dee-969c-1918c6edb5d4/transactions
HTTP/2 200
```

> The above command returns JSON structured like this:

```json
{
    "block": 2546646,
    "chain_id": "22",
    "height": null,
    "last_block_at": 1539384240093,
    "peer_count": 0,
    "protocol_version": null,
    "state": null,
    "syncing": false,
    "meta": {
        "average_blocktime": 5.164322580645161,
        "blocktimes": [
            5.032,
            ...
            5.085
        ],
        "last_block_hash": "0xb6836eed97fd2961832f450b0b3aca0ea0df956f9c28cd5a6e281f2de483938d",
        "last_block_header": {
            "parentHash": "0x48a19fb89487ad54990840a19c06467ab0e06b01e407f13f68bc6eb70b25e83f",
            "sha3Uncles": "0x1dcc4de8dec75d7aab85b567b6ccd41ad312451b948a7413f0a142fd40d49347",
            "miner": "0x9077f27fdd606c41822f711231eeda88317aa67a",
            "stateRoot": "0x38b2dba574c7519e18af5eff4f545d7361ee497677449b4701a0d21200c5643f",
            "transactionsRoot": "0x56e81f171bcc55a6ff8345e692c0f86e5b48e01b996cadc001622fb5e363b421",
            "receiptsRoot": "0x56e81f171bcc55a6ff8345e692c0f86e5b48e01b996cadc001622fb5e363b421",
            "logsBloom": "0x0000000000000000000000000000000000000000000000000000000000000000000...",
            "difficulty": "0xfffffffffffffffffffffffffffffffe",
            "number": "0x26dbd6",
            "gasLimit": "0x47b760",
            "gasUsed": "0x0",
            "timestamp": "0x5bc123b0",
            "extraData": "0xd583010b058650617269747986312e32372e30826c69",
            "mixHash": "0x0000000000000000000000000000000000000000000000000000000000000000",
            "nonce": "0x0000000000000000",
            "hash": "0xb6836eed97fd2961832f450b0b3aca0ea0df956f9c28cd5a6e281f2de483938d"
        }
    }
}
```

This endpoint checks the status of the given Network..


#### HTTP Request

`GET /api/v1/networks/:id/status`

#### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the specific network

## Prices
### Get Prices

```shell
curl -i \
    -H 'Authorization: bearer yoUr-AutH-TOKeN-FrOm-sIgnINg-in' \
    https://goldmine.provide.services/api/v1/prices
HTTP/2 200
```

> The above command returns JSON structured like this:

```json
{
    "btcusd": 14105.2,
    "ethusd": 707,
    "ltcusd": 244.48,
    "prvdusd": 0.42
}
```

This endpoint retrieves real-time pricing data for major currency pairs and supported tokens.


#### HTTP Request

`GET /api/v1/prices`


## Connectors
### Get Connectors


```shell
curl -i \
    -H 'Authorization: bearer an-apPliCaTIOn-aPi-tOkEn' \
    https://goldmine.provide.services/api/v1/connectors
HTTP/2 200
```

> The above command returns JSON structured like this:

```json
{
        "id": "9e5e269a-f074-49e2-8383-ab94a33ae30a",
        "created_at": "2018-10-15T03:18:07.942554Z",
        "application_id": "25b6339c-f11f-4a00-94d7-0a6e9b64586d",
        "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
        "name": "ABC Corp Private IPFS Endpoint",
        "type": "ipfs",
        "config": {
            "gateway_url": "http://ec2-54-175-49-39.compute-1.amazonaws.com:8080",
            "rpc_url": "http://ec2-54-175-49-39.compute-1.amazonaws.com:5001"
        },
        "accessed_at": null
    }
```

This endpoint enumerates configured Connectors.

#### HTTP Request

`GET /api/v1/connectors`

### Configure a new Connector

```shell
curl -i \
    -H 'Authorization: bearer an-apPliCaTIOn-aPi-tOkEn' \
    https://goldmine.provide.services/api/applications/25b6339c-f11f-4a00-94d7-0a6e9b64586d/connectors \
    -d '{"network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
          "application_id": "25b6339c-f11f-4a00-94d7-0a6e9b64586d",
          "type": "ipfs",
          "name": "ABC Corp Private IPFS Endpoint",
          "config": {
            "gateway_url": "http://ec2-54-175-49-39.compute-1.amazonaws.com:8080",
            "rpc_url": "http://ec2-54-175-49-39.compute-1.amazonaws.com:5001"
          }
        }'
HTTP/2 201
```

> The above command returns JSON structured like this:

```json
{
  "id": "9e5e269a-f074-49e2-8383-ab94a33ae30a",
  "created_at": "2018-10-15T03:18:07.942553712Z",
  "application_id": "25b6339c-f11f-4a00-94d7-0a6e9b64586d",
  "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
  "name": "ABC Corp Private IPFS Endpoint",
  "type": "ipfs",
  "config": {
    "gateway_url": "http://ec2-54-175-49-39.compute-1.amazonaws.com:8080",
    "rpc_url": "http://ec2-54-175-49-39.compute-1.amazonaws.com:5001"
  },
  "accessed_at": null
}
```

This endpoint configures a new Connector.


#### HTTP Request

`POST /api/v1/connectors`


### Get details for a Specific Connector

```shell
curl -i \
    -H 'Authorization: bearer an-apPliCaTIOn-aPi-tOkEn' \
    https://goldmine.provide.services/api/v1/connectors/9e5e269a-f074-49e2-8383-ab94a33ae30a
HTTP/2 501
```

> The above command returns JSON structured like this:

```json
{
    "message": "not implemented"
}
```

This endpoint retrieves the details for the specified Connector.

<i> (Not yet implemented) </i>

#### HTTP Request

`GET /api/v1/connectors/:id`

#### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the specific network

### Delete a Specific Connector

```shell
curl -i -XDELETE \
    -H 'Authorization: bearer an-apPliCaTIOn-aPi-tOkEn' \
    https://goldmine.provide.services/api/v1/connectors/9e5e269a-f074-49e2-8383-ab94a33ae30a
HTTP/2 204
```


This endpoint removes the specified Connector.


#### HTTP Request

`DELETE /api/v1/connectors/:id`

#### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the specific network

## Contracts
### Get Contracts


```shell
curl -i \
    -H 'Authorization: bearer yoUr-AutH-TOKeN-FrOm-sIgnINg-in' \
    https://goldmine.provide.services/api/v1/contracts
HTTP/2 200
```

> The above command returns JSON structured like this:

```json
{
        "id": "7ede6b96-874a-424d-ae85-669c1c90dfb8",
        "created_at": "0001-01-01T00:00:00Z",
        "application_id": null,
        "network_id": "4e9e29de-fbd2-4d6a-962e-93bc55c1a306",
        "contract_id": null,
        "transaction_id": null,
        "name": "Network Contract 0x0000000000000000000000000000000000000009",
        "address": "0x0000000000000000000000000000000000000009",
        "params": null,
        "accessed_at": null
    },
    ...
    {
        "id": "652befe6-6cc7-42b2-8994-eeaa98adbf0e",
        "created_at": "0001-01-01T00:00:00Z",
        "application_id": null,
        "network_id": "73c82453-2a19-4f2a-86c6-37f66ae78189",
        "contract_id": null,
        "transaction_id": null,
        "name": "Network Contract 0x0000000000000000000000000000000000000009",
        "address": "0x0000000000000000000000000000000000000009",
        "params": null,
        "accessed_at": null
    }
```

This endpoint enumerates managed smart contracts.


#### HTTP Request

`GET /api/v1/contracts`

#### URL Parameters

Parameter | Default | Description
--------- | ----- | -----------
filter_tokens | true | Filters token contracts from the response

### Deploy a new Contract

```shell
curl -i \
    -H 'Authorization: bearer yoUr-AutH-TOKeN-FrOm-sIgnINg-in' \
    https://goldmine.provide.services/api/contracts \
    -d '{"network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
          "wallet_id": "86ee6d48-66bb-4122-8073-a078854d09e6",
          "data": "0x608060405234...",
          "params": {
            "name": "X12",
            "abi": [
              {
                "constant": false,
                "inputs": [
                  {
                    "name": "sndr_interchange_id",
                    "type": "string"
                  }
                ],
                "name": "send",
                "outputs": [
                ],
                "payable": false,
                "stateMutability": "nonpayable",
                "type": "function"
              }
            ]
          },
          "lang": "bytecode",
          "id": "25b6339c-f11f-4a00-94d7-0a6e9b64586d"
        }'
HTTP/2 201
```

> The above command returns JSON structured like this:

```json
{
  "id": "fccd7404-2eef-4545-a302-5027f60b46d5",
  "created_at": "2018-10-15T03:46:50.138510202Z",
  "application_id": "25b6339c-f11f-4a00-94d7-0a6e9b64586d",
  "user_id": null,
  "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
  "wallet_id": "86ee6d48-66bb-4122-8073-a078854d09e6",
  "to": null,
  "value": 0,
  "data": "0x6080604052...",
  "hash": "0x2bdd0f991...",
  "status": "pending",
  "params": {
    "name": "X12",
    "abi": [
      {
        "constant": false,
        "inputs": [
          {
            "name": "sndr_interchange_id",
            "type": "string"
          },
          ...
          {
            "name": "edi_payload",
            "type": "string"
          }
        ],
        "name": "send",
        "outputs": null,
        "payable": false,
        "stateMutability": "nonpayable",
        "type": "function"
      },
        "name": "makeOffer",
        "outputs": null,
        "payable": false,
        "stateMutability": "nonpayable",
        "type": "function"
      }
    ]
  },
  "traces": null,
  "ref": null,
  "description": null
}
```

This endpoint deploys a new contract.


#### HTTP Request

`POST /api/v1/contracts`


### Get a Specific Contract

```shell
curl -i \
    -H 'Authorization: bearer an-apPliCaTIOn-aPi-tOkEn' \
    https://goldmine.provide.services/api/v1/contracts/55271393-34c7-4d53-8aa8-4a4b06554c1a
HTTP/2 200
```

> The above command returns JSON structured like this:

```json
{
    "id": "55271393-34c7-4d53-8aa8-4a4b06554c1a",
    "created_at": "2018-09-21T14:23:19.926668Z",
    "application_id": "25b6339c-f11f-4a00-94d7-0a6e9b64586d",
    "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
    "contract_id": null,
    "transaction_id": "4bca28a4-7c11-44c0-aba3-acc360421a05",
    "name": "X12",
    "address": "0x61D0deE3E758d73D411c04364bCD56606b1fB833",
    "params": {
        "abi": [
            {
                "constant": false,
                "inputs": [
                    {
                        "name": "sndr_interchange_id",
                        "type": "string"
                    },
                    ...
                    {
                        "name": "edi_payload",
                        "type": "string"
                    }
                ],
                "name": "send",
                "outputs": null,
                "payable": false,
                "stateMutability": "nonpayable",
                "type": "function"
            },
            {
                "constant": true,
                "inputs": null,
                "name": "ipfs_fields",
                "outputs": [
                    {
                        "name": "",
                        "type": "bytes32[]"
                    }
                ],
                "payable": false,
                "stateMutability": "pure",
                "type": "function"
            },
            {
                "constant": true,
                "inputs": null,
                "name": "fave_field",
                "outputs": [
                    {
                        "name": "",
                        "type": "bytes32"
                    }
                ],
                "payable": false,
                "stateMutability": "pure",
                "type": "function"
            }
        ],
        "name": "X12"
    },
    "accessed_at": "2018-10-13T05:29:58.539991Z"
}
```

This endpoint retrieves details for the specified Contract.


#### HTTP Request

`GET /api/v1/contracts/:id`

#### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the specific contract

### Execute a Specific Contract

```shell
curl -i \
     -H 'content-type: application/json' \
     -H 'authorization: bearer an-apPliCaTIOn-aPi-tOkEn' \
     https://goldmine.provide.services/api/v1/contracts/3b9fe62e-5da7-43dc-838f-3cfa1421ed0f/execute \
     -d '{"wallet_id": "a-signing-identity-identifier", "method": "a_method_from_the_contract", "params": ["arguments", "for", "the", "method"], "value": 0.5}'
HTTP/2 202
```

> The above command returns JSON structured like this:

```json
{
    "ref": "specifics-depend-on-the-nature-of-the-contract-and-method"
}
```

This endpoint executes specific functionality encapsulated within a given Contract.


#### HTTP Request

`POST /api/v1/contracts/:id/execute`

### Request Body details

- `wallet_id` is the signing identity to use for the request
- `method` is the function name from the contract to invoke
- `params` is an array of values to pass as arguments to the method
- `value` is the amount of token transfer

#### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the specific contract


## Oracles
### Get Oracles

```shell
curl -i \
     -H 'content-type: application/json' \
     -H 'authorization: bearer an-apPliCaTIOn-aPi-tOkEn' \
     https://goldmine.provide.services/api/v1/oracles
HTTP/2 200
```

> The above command returns JSON structured like this:


This endpoint enumerates managed oracle contracts.


#### HTTP Request

`GET /api/v1/oracles`


### Create and deploy an Oracle


This endpoint creates a managed Oracle smart contract and deploys it to a Network. Upon successful deployment, the data feed will be consumed and written onto the ledger associated with the Network.

<i> (Not yet implemented)</i>

#### HTTP Request

`POST /api/v1/oracles`


### Get a Specific Oracle


This endpoint retrieves details for a specific oracle.


#### HTTP Request

`GET /api/v1/oracles/:id`

#### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the specific Oracle


## Tokens
### Get Tokens

```shell
curl -i \
     -H 'content-type: application/json' \
     -H 'authorization: bearer an-apPliCaTIOn-aPi-tOkEn' \
     https://goldmine.provide.services/api/v1/tokens
HTTP/2 200
```

> The above command returns JSON structured like this:

```json
{
    "message": "not implemented"
}
```

This endpoint enumerates managed Token contracts.

#### HTTP Request

`GET /api/v1/tokens`


### Create a Token


This endpoint creates a new Token.

<i>(Not yet implemented)</i>

#### HTTP Request

`POST /api/v1/tokens`


### Get details for a Specific Token

```curl -i \
     -H 'content-type: application/json' \
     -H 'authorization: bearer an-apPliCaTIOn-aPi-tOkEn' \
     https://goldmine.provide.services/api/v1/tokens/52d9caf3-0a56-4670-886e-8136b633d52b
HTTP/2 501
```

> The above command returns JSON structured like this:

```json
{
    "message": "not implemented"
}
```

This endpoint retrieves details for a specific Token.


#### HTTP Request

`GET /api/v1/tokens/:id`

#### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the specific Token


## Transactions
### Get Transactions


```shell
curl -i \
     -H 'content-type: application/json' \
     -H 'authorization: bearer an-apPliCaTIOn-aPi-tOkEn' \
     https://goldmine.provide.services/api/v1/transactions
HTTP/2 200
```

> The above command returns JSON structured like this:

```json
{
        "id": "fb4c5912-628f-4d8e-9c67-76d379010a71",
        "created_at": "2018-10-03T20:48:37.292823Z",
        "application_id": "e49302c5-e485-4e14-9b0f-db5643b6a15c",
        "user_id": null,
        "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
        "wallet_id": "efef1044-4958-43bc-903b-28f2bb938037",
        "to": null,
        "value": 0,
        "data": "0x608060405234801561001057600080fd5b50610704806100206000396000f300608060405260...",
        "hash": "0xf769d96671abfd8c7dfe9b747db1380d1b974d6282833e573900bad7b11e51e5",
        "status": "success",
        "params": null,
        "traces": null,
        "ref": null,
        "description": null
    }
```

This endpoint enumerates transactions.


#### HTTP Request

`GET /api/v1/transactions`


### Post a Transaction using a Wallet

```shell
curl -i \
     -H 'content-type: application/json' \
     -H 'authorization: bearer an-apPliCaTIOn-aPi-tOkEn' \
     https://goldmine.provide.services/api/v1/transactions \
     -d '{"network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4", "wallet_id": "efef1044-4958-43bc-903b-28f2bb938037", "to": "0xfb17cB7bb99128AAb60B1DD103271d99C8237c0d", "value": 0}'
HTTP/2 201
```

> The above command returns JSON structured like this:

```json
{
    "id": "6759791c-71b5-4fb1-bf19-5488a9f9ee1e",
    "created_at": "2018-10-15T04:04:47.903585906Z",
    "application_id": "e49302c5-e485-4e14-9b0f-db5643b6a15c",
    "user_id": null,
    "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
    "wallet_id": "efef1044-4958-43bc-903b-28f2bb938037",
    "to": "0xfb17cB7bb99128AAb60B1DD103271d99C8237c0d",
    "value": 0,
    "data": null,
    "hash": "0xbc2a0fb68c06d5c2fa603fb7131c3922c4b3b19ece56ee8f8a7d241a9064233e",
    "status": "pending",
    "params": null,
    "traces": null,
    "ref": null,
    "description": null
}
```
> If the broadcast transaction represents a contract deployment, a contract will be created implicitly after deployment is confirmed with the Network. The following example represents a Contract creation with provided params specific to the Ethereum network.

```shell
curl -i \
    -H 'authorization: bearer an-apPliCaTIOn-aPi-tOkEn' \
    https://goldmine.provide.services/api/v1/transactions \
    -d '{
  "network_id": "ba02ff92-f5bb-4d44-9187-7e1cc214b9fc",
  "wallet_id": "ce1fa3b8-049e-467b-90d8-53b9a5098b7b",
  "data": "60606040526003805460a060020a60ff021916905560006...",
  "params": {"name": "ProvideToken",
                "abi": [
                  {
                    "constant": true,
                    "inputs": [
                      {
                        "name": "_holder",
                        "type": "address"
                      }
                    ],
                    "name": "tokenGrantsCount",
                    "outputs": [
                      {
                        "name": "index",
                        "type": "uint256"
                      }
                    ],
                    "payable": false,
                    "type": "function"
                  },
                  ...
                  {
                    "anonymous": false,
                    "inputs": [
                      {
                        "indexed": true,
                        "name": "from",
                        "type": "address"
                      },
                      {
                        "indexed": true,
                        "name": "to",
                        "type": "address"
                      },
                      {
                        "indexed": false,
                        "name": "value",
                        "type": "uint256"
                      }
                    ],
                    "name": "Transfer",
                    "type": "event"
                  }
                ]
              }
            }'
HTTP/2 422
```
> The above command returns JSON structured like this:

```json
{
    "id": "6759791c-71b5-4fb1-bf19-5488a9f9ee1e",
    "created_at": "2018-10-15T04:04:47.903585906Z",
    "application_id": "e49302c5-e485-4e14-9b0f-db5643b6a15c",
    "user_id": null,
    "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
    "wallet_id": "efef1044-4958-43bc-903b-28f2bb938037",
    "to": "0xfb17cB7bb99128AAb60B1DD103271d99C8237c0d",
    "value": 0,
    "data": null,
    "hash": "0xbc2a0fb68c06d5c2fa603fb7131c3922c4b3b19ece56ee8f8a7d241a9064233e",
    "status": "pending",
    "params": null,
    "traces": null,
    "ref": null,
    "description": null
}
```


This endpoint prepares and signs a protocol Transaction using a Wallet on behalf of a specific application User and broadcasts the transaction to the public blockchain Network.

Under certain conditions, calling this API will result in a transaction being created which requires lifecycle management (i.e., in the case when a managed Sidechain has been configured to scale micropayment channels and/or coalesce an application’s transactions for on-chain settlement).


#### HTTP Request

`POST /api/v1/transactions`


### Get a specific Transaction

```shell
curl -i \
     -H 'content-type: application/json' \
     -H 'authorization: bearer an-apPliCaTIOn-aPi-tOkEn' \
     https://goldmine.provide.services/api/v1/transactions/fb4c5912-628f-4d8e-9c67-76d379010a71
HTTP/2 200
```

> The above command returns JSON structured like this:

```json
{
    "id": "fb4c5912-628f-4d8e-9c67-76d379010a71",
    "created_at": "2018-10-03T20:48:37.292823Z",
    "application_id": "e49302c5-e485-4e14-9b0f-db5643b6a15c",
    "user_id": null,
    "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
    "wallet_id": "efef1044-4958-43bc-903b-28f2bb938037",
    "to": null,
    "value": 0,
    "data": "0x608060405234801561001057600080fd5b506...",
    "hash": "0xf769d96671abfd8c7dfe9b747db1380d1b97...",
    "status": "success",
    "params": null,
    "traces": {
        "result": [
            {
                "action": {
                    "callType": null,
                    "from": "0xac805f1c2bf9a19b448bc207075b992be29bc91a",
                    "gas": "0x57caf",
                    "init": "0x608060405234801561001057600080f...",
                    "input": null,
                    "to": null,
                    "value": "0x0"
                },
                "blockHash": "0x4a5e8e1bf594dc4df5c54c4b9c91f...",
                "blockNumber": 2389804,
                "result": {
                    "address": "0x2a3d64307a551a1f2902867f5b2437bc52f0c5c4",
                    "code": "0x6080604052600436106100565763ffffffff7c010000000...",
                    "gasUsed": "0x57caf",
                    "output": null
                },
                "error": null,
                "subtraces": 0,
                "traceAddress": [],
                "transactionHash": "0xf769d96671abfd8c7dfe9b747db138...",
                "transactionPosition": 0,
                "type": "create"
            }
        ]
    },
    "ref": null,
    "description": null
}
```

This endpoint retrieves details for a specific Transaction.



#### HTTP Request

`GET /api/v1/transactions/:id`

#### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the specific Transaction


## Wallets
### Get Wallets

```shell
curl -i \
     -H 'content-type: application/json' \
     -H 'authorization: bearer an-apPliCaTIOn-aPi-tOkEn' \
     https://goldmine.provide.services/api/v1/wallets
HTTP/2 200
```

> The above command returns JSON structured like this:

```json
{
        "id": "efef1044-4958-43bc-903b-28f2bb938037",
        "created_at": "2018-10-03T20:48:03.24878Z",
        "application_id": "e49302c5-e485-4e14-9b0f-db5643b6a15c",
        "user_id": null,
        "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
        "address": "0xAC805F1c2Bf9a19b448bc207075B992Be29bC91a",
        "balance": null,
        "accessed_at": "2018-10-03T20:48:37.291739Z"
    }
```

This endpoint enumerates wallets used for storing cryptocurrency or tokens on behalf of Provide users managing cryptographic material (i.e., for signing transactions).

<aside class="warning">Balances are returned as null here for performance reasons; see  <code>GET /api/v1/wallets/:id</code> to get balance details in the native currency for the network.</aside>

#### HTTP Request

`GET /api/v1/wallets`



### Create a Wallet

```shell
curl -i \
     -H 'content-type: application/json' \
     -H 'authorization: bearer an-apPliCaTIOn-aPi-tOkEn' \
     https://goldmine.provide.services/api/v1/wallets \
     -d '{"network_id":"024ff1ef-7369-4dee-969c-1918c6edb5d4"}'
HTTP/2 201
```

> The above command returns JSON structured like this:

```json
{
    "id": "4059f749-55ad-4c1c-975d-6c5040801079",
    "created_at": "2018-10-12T21:47:13.698524641Z",
    "application_id": "e49302c5-e485-4e14-9b0f-db5643b6a15c",
    "user_id": null,
    "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
    "address": "0xa4f8874C971EB257C0Fd8e33401b274e2a27133d",
    "balance": null,
    "accessed_at": null
}
```

This endpoint creates a managed Wallet (signing identity) capable of storing cryptocurrencies native to a specified Network.


#### HTTP Request

`POST /api/v1/wallets`


### Get a Specific Wallet

```shell
curl -i \
     -H 'content-type: application/json' \
     -H 'authorization: bearer an-apPliCaTIOn-aPi-tOkEn' \
     https://goldmine.provide.services/api/v1/wallets/efef1044-4958-43bc-903b-28f2bb938037
HTTP/2 200
```

> The above command returns JSON structured like this:

```json
{
    "id": "efef1044-4958-43bc-903b-28f2bb938037",
    "created_at": "2018-10-03T20:48:03.24878Z",
    "application_id": "e49302c5-e485-4e14-9b0f-db5643b6a15c",
    "user_id": null,
    "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
    "address": "0xAC805F1c2Bf9a19b448bc207075B992Be29bC91a",
    "balance": 0,
    "accessed_at": "2018-10-03T20:48:37.291739Z"
}
```

This endpoint retrieves Network-specific details for a specific Wallet.



#### HTTP Request

`GET /api/v1/wallets/:id`

#### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the specific wallet

### Get Wallet balance by Contract


This endpoint retrieves details of a specific Wallet's balance by token contract.

<i>(Not yet implemented)</i>

#### HTTP Request

`GET /api/v1/wallets/:id/balances/:tokenId`

#### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the specific wallet
tokenId | The ID of the specific token contract
