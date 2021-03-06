## ResponsePersonalInvoiceFinancingsList
<a id="schemaResponsePersonalInvoiceFinancingsList"></a>

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
          "personalInvoiceFinancings": [
            {
              "type": "string",
              "fees": [{
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
              }],
              "interestRate": {
                "applications": [
                  {
                    "interval": "string",
                    "rate": "string"
                  }
                ],
                "minimumRate": "string",
                "maximumRate": "string"
              },
              "requiredWarranties": [
                "string"
              ],
              "termsConditions": "string"
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

|     Nome      |  Tipo                                                                     | Obrigatório  |                            Definição                  |
|:------------  |:---------------------------------                                         |:-----------  |:----------------------------------------------------  |
| data          | object                                                                    | Sim          |                                                       |
| » brand       | [[PersonalInvoiceFinancingsBrand](#schemaPersonalInvoiceFinancingsBrand)] | Sim          | Lista das organizaçõs titulares das dependências      |
| links         | [[LinksPaginated](#schemaLinksPaginated)]                                 | Sim          |                                                       |
| meta          | [MetaPaginated](#schemaMetaPaginated)                                     | Sim          |                                                       |

## PersonalInvoiceFinancingsBrand
<a id="schemaPersonalInvoiceFinancingsBrand"></a>

```json
{
  "name": "string",
  "companies": [
    {
      "name": "string",
      "cnpjNumber": "string",
      "urlComplementaryList": "string",
      "personalInvoiceFinancings": [
        {
          "type": "string",
          "fees": [{
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
          }],
          "interestRate": {
            "applications": [
              {
                "interval": "string",
                "rate": "string"
              }
            ],
            "minimumRate": "string",
            "maximumRate": "string"
          },
          "requiredWarranties": [
            "string"
          ],
          "termsConditions": "string"
        }
      ]
    }
  ]
}
```

|     Nome     |  Tipo                                                                            | Obrigatório  |                            Definição                         |
|:------------ |:---------------------------------                                                |:-----------  |:----------------------------------------------------         |
| name         | string                                                                           | Sim          | Nome da marca proprietária da dependência (titular).  |
| companies    | [[PersonalInvoiceFinancingsCompanies](#schemaPersonalInvoiceFinancingsCompanies)]  | Sim          | Lista de instituições pertencentes à marca             |

## PersonalInvoiceFinancingsCompanies 
<a id="schemaPersonalInvoiceFinancingsCompanies"></a>

```json
{
  "name": "string",
  "cnpjNumber": "string",
  "urlComplementaryList": "string",
  "personalInvoiceFinancings": [
    {
      "type": "string",
      "fees": [{
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
      }],
      "interestRate": {
        "applications": [
          {
            "interval": "string",
            "rate": "string"
          }
        ],
        "minimumRate": "string",
        "maximumRate": "string"
      },
      "requiredWarranties": [
        "string"
      ],
      "termsConditions": "string"
    }
  ]
}
```

|     Nome                  |  Tipo                                                           | Obrigatório |                            Definição                       |
|:------------              |:-----------------------------------                             |:----------- |:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name                      | string                                                          | Sim         | Nome da Instituição, pertencente à marca, responsável pela comercialização das modalidades de Financiamentos para Pessoas Físicas consultadas. p.ex.'Empresa da Organização A'.         |
| cnpjNumber                | string                                                          | Sim         | CNPJ da instituição responsável                                                                                                                                                         |
| urlComplementaryList      | [[URIString](#commonFieldURIString)]                            | Sim         | URL do link que conterá a lista complementar com os nomes e CNPJs agrupados sob o mesmo cnpjNumber. Os contidos nessa lista possuem as mesmas características para produtos e serviços. |
| personalInvoiceFinancings | [[PersonalInvoiceFinancings](#schemaPersonalInvoiceFinancings)] | Sim         | Lista  de antecipação de recebíveis                                                                                                                                                     |

## PersonalInvoiceFinancings
<a id="schemaPersonalInvoiceFinancings"></a>

```json
{
  "type": "string",
  "fees": [{
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
  }],
  "interestRate": {
    "applications": [
      {
        "interval": "string",
        "rate": "string"
      }
    ],
    "minimumRate": "string",
    "maximumRate": "string"
  },
  "requiredWarranties": [
    "string"
  ],
  "termsConditions": "string"
}
```

|     Nome              |  Tipo                                                                                                       | Obrigatório |                            Definição                                                                                                                                                                                                                                                  |
|:------------          |:---------------------------------------------------------------------------                                 |:----------- |:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------         |
| type                  | [Enum PersonalInvoiceFinancingsType](#schemaEnumPersonalInvoiceFinancingsType)                                | Sim         | Modalidades de direitos creditórios descontados ofertados para pessoas Físicas, conforme Circular 4015-Bacen. Direito creditório descontado é a antecipação de créditos relativos p.ex.: desconto de duplicatas, desconto de cheques, antecipação de fatura de cartão de crédito  |
| fees                  | [[PersonalInvoiceFinancingsFees](#schemaPersonalInvoiceFinancingsFees)]                                       | Sim         | Lista das Tarifas cobradas sobre Serviços ofertados à Modalidade de direitos creditórios descontados, para pessoa física                                                                                                                                                              |
| interestRate         | [[PersonalInvoiceFinancingsInterestRates](#schemaPersonalInvoiceFinancingsInterestRates)]                     | Sim         | Lista de taxas de juros remuneratórias                                                                                                                                                                                                                                                |
| requiredWarranties    | [[Enum PersonalInvoiceFinancingsRequiredWarranties](#schemaEnumPersonalInvoiceFinancingsRequiredWarranties)]  | Sim         | Relação de garantias exigidas                                                                                                                                                                                                                                                         |
| termsConditions       | string                                                                                                        | Não          | Campo aberto para informar as condições contratuais relativas ao produto ou serviço informado. Pode ser informada a URL ([[URIString](#commonFieldURIString)]) referente ao endereço onde constam as condições informadas.   |


### Enum PersonalInvoiceFinancingsType
<a id="schemaEnumPersonalInvoiceFinancingsType"></a>

| Propriedade  | Código                                    | Definição                                             |
|:------------ |:----------------------------------------- |:----------------------------------------------------- |
| type         | DESCONTO_DUPLICATAS                       | Desconto de duplicatas                                |
| type         | DESCONTO_CHEQUES                          | Desconto de cheques                                   |
| type         | ANTECIPACAO_FATURA_CARTAO_CREDITO         | Antecipação de fatura de cartão de crédito            |
| type         | OUTROS_DIREITOS_CREDITORIOS_DESCONTADOS   | Outros direitos creditórios descontados               |
| type         | OUTROS_TITULOS_DESCONTADOS                | Outros títulos descontados                            |


### Enum PersonalInvoiceFinancingsRequiredWarranties
<a id="schemaEnumPersonalInvoiceFinancingsRequiredWarranties"></a>

| Propriedade        | Código                                     | Definição                                             |
|:------------------ |:------------------------------------------ |:----------------------------------------------------- |
| requiredWarranties | CESSAO_DIREITOS_CREDITORIOS                | Cessão de direitos creditórios                        |
| requiredWarranties | CAUCAO                                     | Caução                                                |
| requiredWarranties | PENHOR                                     | Penhor                                                |
| requiredWarranties | ALIENACAO_FIDUCIARIA                       | Alienação fiduciária                                  |
| requiredWarranties | HIPOTECA                                   | Hipoteca                                              |
| requiredWarranties | OPERACOES_GARANTIDAS_GOVERNO               | Operações garantidas pelo governo                     |
| requiredWarranties | OUTRAS_GARANTIAS_NAO_FIDEJUSSORIAS         | Outras garantias não fidejussórias                    |
| requiredWarranties | SEGUROS_ASSEMELHADOS                       | Seguros e assemelhados                                |
| requiredWarranties | GARANTIA_FIDEJUSSORIA                      | Garantia fidejussória                                 |
| requiredWarranties | BENS_ARRENDADOS                            | Bens arrendados                                       |
| requiredWarranties | GARANTIAS_INTERNACIONAIS                   | Garantias internacionais                              |
| requiredWarranties | OPERACOES_GARANTIDAS_OUTRAS_ENTIDADE       | Operações garantidas por outras entidades             |
| requiredWarranties | ACORDOS_COMPENSACAO                        | Acordos de compensação                                |
| requiredWarranties | NAO_APLICAVEL                              | Não aplicável                                         |

## PersonalInvoiceFinancingsFees 
<a id="schemaPersonalInvoiceFinancingsFees"></a>

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

| Nome         |  Tipo                                                                                 | Obrigatório    |  Definição                                                                                                                                 |
|:------------ |:------------------------------------------------------------------------------------- |:-------------- |:------------------------------------------------------------------------------------------------------------------------------------------ |
| service      | [[PersonalInvoiceFinancingsFeesService](#schemaPersonalInvoiceFinancingsFeesService)] | Sim            | Nomes das Tarifas cobradas sobre Serviços ofertados à Modalidade de direitos creditórios descontados, para pessoa física. (Campo Livre)    |

## PersonalInvoiceFinancingsFeesService 
<a id="schemaPersonalInvoiceFinancingsFeesService"></a>

```json
{
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
```

|     Nome             |  Tipo                                  | Obrigatório    |                            Definição                                                                                                       |
|:------------         |:-------------------------------------- |:-------------- |:------------------------------------------------------------------------------------------------------------------------------------------ |
| name                 | string                                 | Sim            | Nomes das Tarifas cobradas sobre Serviços ofertados à Modalidade de direitos creditórios descontados, para pessoa física. (Campo Livre)    |
| code                 | string                                 | Sim            | Sigla de identificação do serviço relacionado à Modalidade de direitos creditórios descontados, para pessoa física. Campo aberto           |
| chargingTriggerInfo  | string                                 | Não            | Fatos geradores de cobrança que incidem sobre as Modalidades de direitos creditórios descontados, para pessoa física. Campo Livre          |
| prices               | [[Price](#schemaPrice)]                | Sim            | Valor da mediana, relativa ao serviço ofertado, informado no período.                                                                      |
| minimum              | [[MinimumPrice](#schemaMinimumPrice)]  | Sim            | Valor mínimo cobrado para a tarifa de serviços sobre a base de clientes no mês de referência.                                              | 
| maximum              | [[MaximumPrice](#schemaMaximumPrice)]  | Sim            | Valor máximo cobrado para a tarifa de serviços sobre a base de clientes no mês de referência.                                              | 

## PersonalInvoiceFinancingsInterestRates 
<a id="schemaPersonalInvoiceFinancingsInterestRates"></a>

```json
{
  "applications": [
    {
      "interval": "string",
      "rate": "string"
    }
  ],
  "minimumRate": "string",
  "maximumRate": "string"
}
```

|  Nome           |  Tipo                   | Obrigatório |   Definição   |
|:--------------- |:----------------------- |------------ |:--------------|
| applications    | [[Price](#schemaPrice)] | Sim | Valor da mediana da taxa de remuneração relativa ao serviço ofertado, para pessoa física informado no período.     
| minimumRate     | string                  | Sim | Valor mínimo cobrado para a taxa de remuneração relativa ao serviço ofertado, sobre a base de clientes,  no mês de referência | Este campo deve estar obrigatoriamente preenchido se não houver conteúdo para os itens: value, currency e type
| maximumRate     | string                  | Sim | Valor máximo cobrado para a taxa de remuneração relativa ao serviço ofertado, sobre a base de clientes,  no mês de referência | Este campo deve estar obrigatoriamente preenchido se não houver conteúdo para os itens: value, currency e type
