## ResponseBusinessCreditCardsList
<a id="schemaResponseBusinessCreditCardsList"></a>

```json
{
  "data": {
    "brand": {
      "name": "string",
      "companies": [
        {
          "name": "string",
          "cnpjNumber": "string",
          "urlComplementaryList": "string",
          "businessCreditCards": [
            {
              "name": "string",
              "identification": {
                "product": {
                  "type": "string",
                  "additionalInfo": "string"
                },
                "creditCard": {
                  "network": "string",
                  "additionalInfo": "string"
                }
              },
              "rewardsProgram": {
                "hasRewardProgram": "string",
                "rewardProgramInfo": "string"
              },
              "fees": [
                {
                  "service": {
                    "name": "string",
                    "code": "string",
                    "chargingTriggerInfo": "string",
                    "prices": [
                      {
                        "interval": "string",
                        "value": "string",
                        "currency": "string"
                      }
                    ],
                    "minimum": {
                      "value": "string",
                      "currency": "string"
                    },
                    "maximum": {
                      "value": "string",
                      "currency": "string"
                    }
                  }
                }
              ],
              "interest": {
                "feeRate": {
                  "prices": [
                    [
                      {
                        "interval": "string",
                        "rate": "string"
                      }
                    ]
                  ],
                  "minimumRate": "string",
                  "maximumRate": "string"
                },
                "instalmentRate": {
                  "prices": [
                    [
                      {
                        "interval": "string",
                        "rate": "string"
                      }
                    ]
                  ],
                  "minimumRate": "string",
                  "maximumRate": "string"
                },
                "interestRates": [{
                  "code": "string",
                  "additionalInfo": "string",
                  "prices": [
                    [
                      {
                        "interval": "string",
                        "rate": "string"
                      }
                    ]
                  ],
                  "minimumRate": "string",
                  "maximumRate": "string"
                }]
              },
              "termsConditions": {
                "minimumFeeRate": "string",
                "additionalInfo": "string",
                "elegibilityCriteriaInfo": "string",
                "closingProcessInfo": "string"
              }
            }
          ]
        }
      ]
    }
  },
  "links": {
    "self": "string",
    "first": "string",
    "prev": "string",
    "next": "string",
    "last": "string"
  },
  "meta": {
    "totalRecords": "integer",
    "totalPages": "integer"
  }
}
```

|     Nome          |  Tipo                                                       | Obrigatório  |                            Definição                                                                      |
|:------------------|:----------------------------------------------------------- |:------------ |:--------------------------------------------------------------------------------------------------------- | 
| data              | object                                                      | Sim          |                                                                                                           |
| » brand           | [BusinessCreditCardBrand](#schemaBusinessCreditCardBrand) | Sim          | Dados da Marca selecionada que fornecem produtos e serviços de cartões de crédito para pessoa jurídica    |
| links             | [LinksPaginated](#schemaLinksPaginated)                     | Sim          |                                                                                                           |
| meta              | [MetaPaginated](#schemaMetaPaginated)                       | Sim          |                                                                                                           |

## BusinessCreditCardBrand
<a id="schemaBusinessCreditCardBrand"></a>

```json
{
  "name": "string",
  "companies": [
    {
      "name": "string",
      "cnpjNumber": "string",
      "urlComplementaryList": "string",
      "businessCreditCards": [
        {
          "name": "string",
          "identification": {
            "product": {
              "type": "string",
              "additionalInfo": "string"
            },
            "creditCard": {
              "network": "string",
              "additionalInfo": "string"
            }
          },
          "rewardsProgram": {
            "hasRewardProgram": "string",
            "rewardProgramInfo": "string"
          },
          "fees": [
            {
              "service": {
                "name": "string",
                "code": "string",
                "chargingTriggerInfo": "string",
                "prices": [
                  {
                    "interval": "string",
                    "value": "string",
                    "currency": "string"
                  }
                ],
                "minimum": {
                  "value": "string",
                  "currency": "string"
                },
                "maximum": {
                  "value": "string",
                  "currency": "string"
                }
              }
            }
          ],
          "interest": {
            "feeRate": {
              "prices": [
                [
                  {
                    "interval": "string",
                    "rate": "string"
                  }
                ]
              ],
              "minimumRate": "string",
              "maximumRate": "string"
            },
            "instalmentRate": {
              "prices": [
                [
                  {
                    "interval": "string",
                    "rate": "string"
                  }
                ]
              ],
              "minimumRate": "string",
              "maximumRate": "string"
            },
            "interestRates": [{
              "code": "string",
              "additionalInfo": "string",
              "prices": [
                [
                  {
                    "interval": "string",
                    "rate": "string"
                  }
                ]
              ],
              "minimumRate": "string",
              "maximumRate": "string"
            }]
          },
          "termsConditions": {
            "minimumFeeRate": "string",
            "additionalInfo": "string",
            "elegibilityCriteriaInfo": "string",
            "closingProcessInfo": "string"
          }
        }
      ]
    }
  ]
}
```

|     Nome     |  Tipo                                                                    | Obrigatório  |                            Definição                 |
|:-------------|:-------------------------------------------------------------------------|:-----------  |:---------------------------------------------------- |
| name         | string                                                                   | Sim          | Nome da Marca selecionada pelas Organizações         |
| companies    | [[BusinessCreditCardCompanies](#schemaBusinessCreditCardCompanies)]    | Sim          | Lista de instituições pertencentes a marca           |

## BusinessCreditCardCompanies 
<a id="schemaBusinessCreditCardCompanies"></a>

```json
{
  "name": "string",
  "cnpjNumber": "string",
  "urlComplementaryList": "string",
  "businessCreditCards": [
    {
      "name": "string",
      "identification": {
        "product": {
          "type": "string",
          "additionalInfo": "string"
        },
        "creditCard": {
          "network": "string",
          "additionalInfo": "string"
        }
      },
      "rewardsProgram": {
        "hasRewardProgram": "string",
        "rewardProgramInfo": "string"
      },
      "fees": [
        {
          "service": {
            "name": "string",
            "code": "string",
            "chargingTriggerInfo": "string",
            "prices": [
              {
                "interval": "string",
                "value": "string",
                "currency": "string"
              }
            ],
            "minimum": {
              "value": "string",
              "currency": "string"
            },
            "maximum": {
              "value": "string",
              "currency": "string"
            }
          }
        }
      ],
      "interest": {
        "feeRate": {
          "prices": [
            [
              {
                "interval": "string",
                "rate": "string"
              }
            ]
          ],
          "minimumRate": "string",
          "maximumRate": "string"
        },
        "instalmentRate": {
          "prices": [
            [
              {
                "interval": "string",
                "rate": "string"
              }
            ]
          ],
          "minimumRate": "string",
          "maximumRate": "string"
        },
        "interestRates": [{
          "code": "string",
          "additionalInfo": "string",
          "prices": [
            [
              {
                "interval": "string",
                "rate": "string"
              }
            ]
          ],
          "minimumRate": "string",
          "maximumRate": "string"
        }]
      },
      "termsConditions": {
        "minimumFeeRate": "string",
        "additionalInfo": "string",
        "elegibilityCriteriaInfo": "string",
        "closingProcessInfo": "string"
      }
    }
  ]
}
```

|     Nome             |  Tipo                                                | Obrigatório    |    Definição                       |
|:---------------------|:-----------------------------------------------------|:-------------- |:-----------------------------------|
| name                 | string                                               | Sim            | Nome da instituição financeira     |
| cnpjNumber           | string                                               | Sim            | CNPJ da instituição financeira     |
| urlComplementaryList | string                                               | Não            | URL do link que conterá a lista complementar com os nomes e CNPJs agrupados sob o mesmo cnpjNumber |
| businessCreditCards  | [[BusinessCreditCard](#schemaBusinessCreditCard)]  | Sim            | Lista  de cartões de crédito       |

## BusinessCreditCard
<a id="schemaBusinessCreditCard"></a>

```json
{
  "name": "string",
  "identification": {
    "product": {
      "type": "string",
      "additionalInfo": "string"
    },
    "creditCard": {
      "network": "string",
      "additionalInfo": "string"
    }
  },
  "rewardsProgram": {
    "hasRewardProgram": "string",
    "rewardProgramInfo": "string"
  },
  "fees": [
    {
      "service": {
        "name": "string",
        "code": "string",
        "chargingTriggerInfo": "string",
        "prices": [
          {
            "interval": "string",
            "value": "string",
            "currency": "string"
          }
        ],
        "minimum": {
          "value": "string",
          "currency": "string"
        },
        "maximum": {
          "value": "string",
          "currency": "string"
        }
      }
    }
  ],
  "interest": {
    "feeRate": {
      "prices": [
        [
          {
            "interval": "string",
            "rate": "string"
          }
        ]
      ],
      "minimumRate": "string",
      "maximumRate": "string"
    },
    "instalmentRate": {
      "prices": [
        [
          {
            "interval": "string",
            "rate": "string"
          }
        ]
      ],
      "minimumRate": "string",
      "maximumRate": "string"
    },
    "interestRates": [{
      "code": "string",
      "additionalInfo": "string",
      "prices": [
        [
          {
            "interval": "string",
            "rate": "string"
          }
        ]
      ],
      "minimumRate": "string",
      "maximumRate": "string"
    }]
  },
  "termsConditions": {
    "minimumFeeRate": "string",
    "additionalInfo": "string",
    "elegibilityCriteriaInfo": "string",
    "closingProcessInfo": "string"
  }
}
```

|     Nome              |  Tipo                                                                             | Obrigatório |                            Definição                                      |
|:----------------------|:----------------------------------------------------------------------------------|:------------|:--------------------------------------------------------------------------|
| name                  | string                                                                            | Sim         | Denominação/Identificação do nome da conta (cartão de crédito)            |
| identification        | [BusinessCreditCardIdentification](#schemaBusinessCreditCardIdentification)                     | Sim         | Informações de identificação do cartão de crédito                         |
| rewardsProgram        | [BusinessCreditCardRewardProgram](#schemaBusinessCreditCardRewardProgram)     | Sim         | Informações sobre programas de recompensa presentes no cartão de crédito  |
| fees                  | [BusinessCreditCardFee](#schemaBusinessCreditCardFee)                         | Sim         | Informações sobre tarifas cobradas sobre o produto e serviços             |
| interest              | [BusinessCreditCardInterest](#schemaBusinessCreditCardInterest)       | Sim         | Informações sobre taxas de juros                                          |
| termsConditions       | [BusinessCreditCardTermsConditions](#schemaBusinessCreditCardTermsConditions)   | Sim         | Informações sobre termos e condições para aquisição e cancelamento        |


## BusinessCreditCardIdentification
<a id="schemaBusinessCreditCardIdentification"></a>

```json
{
  "product":{
    "type": "string",
    "additionalInfo": "string"
  },
  "creditCard":{
    "network": "string",
    "additionalInfo": "string",
  }
}
```

|     Nome          |  Tipo        | Obrigatório    |    Definição                   |
|:----------------- |:------------ |:-------------- |:------------------------------ |
| product           | [BusinessCreditCardIdentificationProduct](#schemaBusinessCreditCardIdentificationProduct)       | Sim            | Categoria atribuída a um cartão de pagamento, sob uma certa denominação, que lhe agrega um conjunto de vantagens, diferenciando-o de acordo com o perfil do portador  |
| creditCard        | [BusinessCreditCardIdentificationCreditCard](#schemaBusinessCreditCardIdentificationCreditCard) | Sim            | Categoria de Bandeiras de Cartões de Crédito |

## BusinessCreditCardIdentificationProduct
<a id="schemaBusinessCreditCardIdentificationProduct"></a>

```json
{
  "type": "string",
  "additionalInfo": "string"
}
```

|     Nome          |  Tipo        | Obrigatório    |    Definição                   |
|:----------------- |:------------ |:-------------- |:------------------------------ |
| type              | [Enum BusinessCreditCardProductType](#schemaEnumBusinessCreditCardProductType) | Sim  | Categoria atribuída a um cartão de pagamento, sob uma certa denominação, que lhe agrega um conjunto de vantagens, diferenciando-o de acordo com o perfil do portador. Essa categoria é definida pelo BACEN e está contida no documento de nome 'Elaboração e Remessa de Informações Relativas aos Cartões de Pagamento  Emissores' |
| additionalInfo    | string                                                                         | Sim  | Texto livre para especificar                              |

### Enum BusinessCreditCardProductType
<a id="schemaEnumBusinessCreditCardProductType"></a>

| Propriedade         | Código                     | Definição                  |
|:------------------- |:-------------------------- |:-------------------------- |
| productType         | CLASSIC_NACIONAL           | Classic Nacional           |
| productType         | CLASSIC_INTERNACIONAL      | Classic Internacional      |
| productType         | GOLD                       | Gold                       |
| productType         | PLATINUM                   | Platinum                   |
| productType         | INFINITE                   | Infinite                   |
| productType         | ELECTRON                   | Electron                   |
| productType         | STANDARD_NACIONAL          | Standard Nacional          |
| productType         | STANDARD_INTERNACIONAL     | Standard Internacional     |
| productType         | ELETRONIC                  | Classic Nacional           |
| productType         | BLACK                      | Classic Internacional      |
| productType         | REDESHOP                   | Gold                       |
| productType         | MAESTRO_MASTERCARD_MAESTRO | Maestro Mastercard maestro |
| productType         | GREEN                      | green                      |
| productType         | BLUE                       | blue                       |
| productType         | BLUEBOX                    | blue box                   |
| productType         | PROFISSIONAL_LIBERAL       | profissional liberal       |
| productType         | CHEQUE_ELETRONICO          | cheque eletronico          |
| productType         | CORPORATIVO                | corporativo                |
| productType         | EMPRESARIAL                | Empresarial                |
| productType         | COMPRAS                    | compras                    |
| productType         | OUTROS                     | outros                     |

## BusinessCreditCardIdentificationCreditCard
<a id="schemaBusinessCreditCardIdentificationCreditCard"></a>

```json
{
  "network": "string",
  "additionalInfo": "string",
}
```

|     Nome          |  Tipo        | Obrigatório    |    Definição                   |
|:----------------- |:------------ |:-------------- |:------------------------------ |
| network           | [Enum BusinessCreditCardBrandCode](#schemaEnumBusinessCreditCardBrandCode) | Sim            | Categoria de Bandeiras de Cartões. Bandeira é a detentora de todos os direitos e deveres da utilização da marca estampada no cartão, inclusive as bandeiras pertencentes aos emissores. Essas bandeiras estão definidas em documento do BACEN de nome 'Elaboração e Remessa de Informações Relativas aos Cartões de Pagamento  Emissores' |
| additionalInfo    | string                                                                     | Sim            | Texto livre para especificar categoria de bandeira marcada como 'Outras' |

### Enum BusinessCreditCardBrandCode
<a id="schemaEnumBusinessCreditCardBrandCode"></a>

| Propriedade       | Código            | Definição           |
|:------------------|:------------------|:------------------- |
| creditCardNetwork | VISA              | Visa                |
| creditCardNetwork | MASTERCARD        | MasterCard          |
| creditCardNetwork | AMERICAN_EXPRESS  | American Express    |
| creditCardNetwork | DINERS_CLUB       | Diners Club         |
| creditCardNetwork | HIPERCARD         | Hipercard           |
| creditCardNetwork | BANDEIRA_PROPRIA  | Bandeira própria    |
| creditCardNetwork | CHEQUE_ELETRONICO | Cheque Eletrônico   |
| creditCardNetwork | ELO               | Elo                 |
| creditCardNetwork | OUTRAS            | Outras              |

## BusinessCreditCardRewardProgram
<a id="schemaBusinessCreditCardRewardProgram"></a>

```json
{
  "hasRewardProgram": "boolean",
  "rewardProgramInfo": "string"
}
```

|     Nome            |  Tipo           | Obrigatório     |    Definição                                                                                                                                                  |
|:--------------------|:--------------- |:--------------  |:------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| hasRewardProgram    | boolean         | Sim             | Indicador da existência de programa de fidelidade/recompensa associado à conta                                                                                |
| rewardProgramInfo   | string          | Não             | Informações de termos e condições do programa de fidelidade/recompensa. Pode ser informada a URL referente ao endereço onde constam as condições informadas   |

## BusinessCreditCardFee
<a id="schemaBusinessCreditCardFee"></a>

```json
{
  "service": {
    "name": "string",
    "code": "string",
    "chargingTriggerInfo": "string",
    "prices": [
        {
          "interval": "string",
          "value": "string",
          "currency": "string"
        }
      ],
      "minimum": {
        "value": "string",
        "currency": "string"
      },
      "maximum": {
        "value": "string",
        "currency": "string"
      }
  }
}
```

|     Nome    |  Tipo                                                               | Obrigatório     |    Definição                           |
|:------------|:--------------------------------------------------------------------|:----------------|:-------------------------------------- |
| services    | [[BusinessCreditCardService](#schemaBusinessCreditCardService)]     | Sim             | Informações de tarifas sobre serviços  |

## BusinessCreditCardService
<a id="schemaBusinessCreditCardService"></a>

```json
{
  "name": "string",
  "code": "string",
  "chargingTriggerInfo": "string",
  "price": [
    {
      "interval": "string",
      "value": "string",
      "currency": "string"
    }
  ],
  "minimum": {
    "value": "string",
    "currency": "string"
  },
  "maximum": {
    "value": "string",
    "currency": "string"
  }
}
```

|     Nome   |  Tipo  | Obrigatório     |    Definição   |
|:---------- |:-------|:----------------|:-------------- |
| name                | string                                | Sim | Nomes das Tarifas cobradas sobre Serviços relacionados à Modalidade informada de Contas de Pagamento Pós-Pagas para pessoa jurídica               |
| code                | string                                | Sim | Fatos geradores de cobrança que incidem sobre as Modalidades de Contas de Pagamento Pós-Pagas informada, para pessoa jurídica.               |
| chargingTriggerInfo | string                                | Sim | Fatos geradores de cobrança que incidem sobre as Modalidades inforrmadas de Contas de Pagamento Pós-Pagas para pessoa jurídica                  |
| price               | [[Price](#schemaPrice)]               | Sim | Informações sobre a tarifa cobrada, relativa ao serviço relacionado à Modalidade informada de Contas de Pagamento Pós-Pagas para pessoa jurídica  |
| minimum             | [[MinimumPrice](#schemaMinimumPrice)] | Sim | Valor mínimo cobrado para a taxa de remuneração relativa ao serviço ofertado sobre a base de clientes no mês de referência. Este campo deve estar obrigatoriamente preenchido se não houver conteúdo para os itens: value, currency e type
| maximum             | [[MaximumPrice](#schemaMaximumPrice)] | Sim | Valor máximo cobrado para a taxa de remuneração relativa ao serviço ofertado sobre a base de clientes no mês de referência. Este campo deve estar obrigatoriamente preenchido se não houver conteúdo para os itens: value, currency e type |

## BusinessCreditCardInterest
<a id="schemaBusinessCreditCardInterest"></a>

```json
{
  "feeRate": {
    "prices": [
      {
        "interval": "string",
        "rate": "string"
      }
    ],
    "minimumRate": "string",
    "maximumRate": "string"
  },
  "instalmentRate": {
    "prices": [
      {
        "interval": "string",
        "rate": "string"
      }
    ],
    "minimumRate": "string",
    "maximumRate": "string"
  },
  "interestRates": [{
    "code": "string",
    "additionalInfo": "string",
    "prices": [
      {
        "interval": "string",
        "rate": "string"
      }
    ],
    "minimumRate": "string",
    "maximumRate": "string"
  }]
}
```

|     Nome       |  Tipo                       | Obrigatório      |    Definição                                                 |
|:-------------- |:--------------------------- |:---------------- |:------------------------------------------------------------ |
| feeRate        | [BusinessCreditCardFeeRate](#schemaBusinessCreditCardFeeRate)               | Sim | Percentual que corresponde a taxa aplicada para utilização de Crédito Rotativo              |
| instalmentRate | [BusinessCreditCardInstalmentRate](#schemaBusinessCreditCardInstalmentRate) | Sim | Percentual que corresponde a taxa aplicada para pagamento parcelado do saldo devedor quando não realizado pagamento integral da fatura |
| interestRates   | [BusinessCreditCardInterestRate](#schemaBusinessCreditCardInterestRate) | Sim | Percentual que corresponde a taxa aplicada para pagamento parcelado do saldo devedor quando não realizado pagamento integral da fatura |

## BusinessCreditCardInterestRate
<a id="schemaBusinessCreditCardInterestRate"></a>

```json
{
  "code": "string",
  "additionalInfo": "string",
  "prices": [
    {
      "interval": "string",
      "rate": "string"
    }
  ],
  "minimumRate": "string",
  "maximumRate": "string"
}
```

|     Nome        |  Tipo                                                                                       | Obrigatório     |    Definição        |
|:----------------|:--------------------------------------------------------------------------------------------|:----------------|:--------------------|
| code            | [Enum BusinessCreditCardInterestRateCode](#schemaEnumBusinessCreditCardInterestRateCode) | Sim    | Lista de outras operações de crédito                                          |
| additionalInfo  | string                                                                                       | Sim    | Campo Texto para descrever outras operações de crédito marcadas como 'Outros' |
| prices           | [[Rate](#schemaRate)]               | Sim    | Informações sobre a tarifa cobrada, relativa ao serviço relacionado à Modalidade informada de Contas de Pagamento Pós-Pagas para pessoa física  |
| minimumRate     | String                              | Sim    | Percentual mínimo cobrado para a taxa do crédito rotativo no mês de referência                                                                  |
| maximumRate     | String                              | Sim    | Percentual máximo cobrado para o pagamento parcelado do saldo devedor na fatura do mês de referência.                                           |

### Enum BusinessCreditCardInterestRateCode
<a id="schemaEnumBusinessCreditCardInterestRateCode"></a>

| Propriedade                 | Código               | Definição        |
|:----------------------------|:---------------------|:------------------- |
| code                        | SAQUE_CREDITO        | Saque a crédito     |
| code                        | PAGAMENTO_CONTA      | Pagamento de contas |
| code                        | OUTROS               | Outros              |


## BusinessCreditCardFeeRate
<a id="schemaBusinessCreditCardFeeRate"></a>

```json
{
  "prices": [
    {
      "interval": "string",
      "rate": "string",
      "frequency": "string"
    }
  ],
  "minimumRate" : "string",
  "maximumRate" : "string"
}
```

|     Nome                |  Tipo       | Obrigatório     |    Definição                                                                                                                                                          |
|:------------------------|:------------|:----------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| prices                 [[Rate](#schemaRate)]                                                                 | Sim             | Informações sobre a tarifa cobrada, relativa ao serviço relacionado à Modalidade informada de Contas de Pagamento Pós-Pagas para pessoa física  |
| minimumRate     | String                                                                                      | Sim             | Percentual mínimo cobrado para a taxa do crédito rotativo no mês de referência                                                                |
| maximumRate     | String                                                                                      | Sim             | Percentual máximo cobrado para o pagamento parcelado do saldo devedor na fatura do mês de referência.                                                                   |

## BusinessCreditCardInstalmentRate
<a id="schemaBusinessCreditCardInstalmentRate"></a>

```json
{
  "prices": [
    {
      "interval": "string",
      "rate": "string",
      "frequency": "string"
    }
  ],
  "minimumRate" : "string",
  "maximumRate" : "string"
}
```

|     Nome     |  Tipo       | Obrigatório     |    Definição        |
|:------------ |:----------- |:--------------- |:------------------- |
| prices        | [[Rate](#schemaRate)] | Sim    | Informações sobre a tarifa cobrada, relativa ao serviço relacionado à Modalidade informada de Contas de Pagamento Pós-Pagas para pessoa física  |
| minimumRate  | String                | Sim    | Percentual mínimo cobrado para a taxa do crédito rotativo no mês de referência                                                                  |
| maximumRate  | String                | Sim    | Percentual máximo cobrado para o pagamento parcelado do saldo devedor na fatura do mês de referência.                                           |

## BusinessCreditCardTermsConditions
<a id="schemaBusinessCreditCardTermsConditions"></a>

```json
{
  "minimumFeeRate": "string",
  "additionalInfo": "string",
  "elegibilityCriteriaInfo": "string",
  "closingProcessInfo": "string"
}
```

|     Nome                |  Tipo                                 | Obrigatório     |    Definição                                                                                                                                                          |
|:------------------------|:------------                          |:----------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| minimumFeeRate          | [RateString](#commonFieldRateString)  | Sim             | Percentual para pagamento mínimo sobre o saldo devedor da fatura                                                                                                      |
| additionalInfo          | string                                | Sim             | Campo aberto para detalhamento de taxas de juros                                                                                                                      |
| elegibilityCriteriaInfo | string                                | Sim             | Informação sobre as condições e critérios de elegibilidade do emissor do cartão. Pode ser informada a URL referente ao endereço onde constam as condições informadas  |
| closingProcessInfo      | string                                | Sim             | Descrição dos procedimentos para encerramento da conta pós paga. Pode ser informada a URL referente ao endereço onde constam as condições informadas                  |