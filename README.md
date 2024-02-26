

## Dataset
- [MultiWOZ - A Large-Scale Multi-Domain Wizard-of-Oz Dataset for Task-Oriented Dialogue Modelling](https://arxiv.org/abs/1810.00278]) ([github](https://github.com/budzianowski/multiwoz/tree/master))
- [Building a Conversational Agent Overnight with Dialogue Self-Play](https://arxiv.org/pdf/1801.04871.pdf)
([dstc8-schema-guided-dialogue](https://github.com/google-research-datasets/dstc8-schema-guided-dialogue))
([simulated-dialogue](https://github.com/google-research-datasets/simulated-dialogue))
---

### slot
- 有限且明確的值
    - categorical slot：有限且明確的值
    - non-categorical slot：無限可能的值
- 是否持續在state中追蹤
    - tracked in the dialogue state：在用戶state中保留
    - requested slot：紀錄用戶當下詢問的資訊但不需保留
- 針對non-categorical slot紀錄span annotations

```
{
    "dialogue_id": "PMUL4398.json",
    "services": [
      "restaurant",
      "hotel"
    ],
    "turns": [
      {
        "frames": [
          {
            "actions": [],
            "service": "restaurant",
            "slots": [],
            "state": {
              "active_intent": "find_restaurant",
              "requested_slots": [],
              "slot_values": {
                "restaurant-area": [
                  "centre"
                ],
                "restaurant-pricerange": [
                  "expensive"
                ]
              }
            }
          }
        ],
        "speaker": "USER",
        "turn_id": "0",
        "utterance": "i need a place to dine in the center thats expensive"
      },
      {
        "frames": [],
        "speaker": "SYSTEM",
        "turn_id": "1",
        "utterance": "I have several options for you; do you prefer African, Asian, or British food?"
      },
      {
        "frames": [
          {
            "actions": [],
            "service": "restaurant",
            "slots": [],
            "state": {
              "active_intent": "find_restaurant",
              "requested_slots": [
                "restaurant-food"
              ],
              "slot_values": {
                "restaurant-area": [
                  "centre"
                ],
                "restaurant-pricerange": [
                  "expensive"
                ]
              }
            }
          },
          {
            "actions": [],
            "service": "hotel",
            "slots": [],
            "state": {
              "active_intent": "find_hotel",
              "requested_slots": [],
              "slot_values": {}
            }
          }
        ],
        "speaker": "USER",
        "turn_id": "2",
        "utterance": "Any sort of food would be fine, as long as it is a bit expensive. Could I get the phone number for your recommendation?"
      },
      {
        "frames": [
          {
            "actions": [],
            "service": "restaurant",
            "slots": [
              {
                "exclusive_end": 38,
                "slot": "restaurant-name",
                "start": 31,
                "value": "Bedouin"
              }
            ]
          }
        ],
        "speaker": "SYSTEM",
        "turn_id": "3",
        "utterance": "There is an Afrian place named Bedouin in the centre. How does that sound?"
      },
      {
        "frames": [
          {
            "actions": [],
            "service": "restaurant",
            "slots": [],
            "state": {
              "active_intent": "find_restaurant",
              "requested_slots": [
                "restaurant-phone"
              ],
              "slot_values": {
                "restaurant-area": [
                  "centre"
                ],
                "restaurant-name": [
                  "bedouin"
                ],
                "restaurant-pricerange": [
                  "expensive"
                ]
              }
            }
          },
          {
            "actions": [],
            "service": "hotel",
            "slots": [],
            "state": {
              "active_intent": "find_hotel",
              "requested_slots": [],
              "slot_values": {
                "hotel-pricerange": [
                  "expensive"
                ],
                "hotel-type": [
                  "hotel"
                ]
              }
            }
          }
        ],
        "speaker": "USER",
        "turn_id": "4",
        "utterance": "Sounds good, could I get that phone number? Also, could you recommend me an expensive hotel?"
      },
      {
        "frames": [
          {
            "actions": [],
            "service": "hotel",
            "slots": [
              {
                "exclusive_end": 90,
                "slot": "hotel-name",
                "start": 69,
                "value": "University Arms Hotel"
              }
            ]
          }
        ],
        "speaker": "SYSTEM",
        "turn_id": "5",
        "utterance": "Bedouin's phone is 01223367660. As far as hotels go, I recommend the University Arms Hotel in the center of town."
      },
      {
        "frames": [
          {
            "actions": [],
            "service": "restaurant",
            "slots": [],
            "state": {
              "active_intent": "NONE",
              "requested_slots": [],
              "slot_values": {
                "restaurant-area": [
                  "centre"
                ],
                "restaurant-name": [
                  "bedouin"
                ],
                "restaurant-pricerange": [
                  "expensive"
                ]
              }
            }
          },
          {
            "actions": [],
            "service": "hotel",
            "slots": [],
            "state": {
              "active_intent": "find_hotel",
              "requested_slots": [],
              "slot_values": {
                "hotel-name": [
                  "university arms hotel"
                ],
                "hotel-pricerange": [
                  "expensive"
                ],
                "hotel-type": [
                  "hotel"
                ]
              }
            }
          }
        ],
        "speaker": "USER",
        "turn_id": "6",
        "utterance": "Yes. Can you book it for me?"
      },
      {
        "frames": [],
        "speaker": "SYSTEM",
        "turn_id": "7",
        "utterance": "Sure, when would you like that reservation?"
      },
      {
        "frames": [
          {
            "actions": [],
            "service": "restaurant",
            "slots": [],
            "state": {
              "active_intent": "NONE",
              "requested_slots": [],
              "slot_values": {
                "restaurant-area": [
                  "centre"
                ],
                "restaurant-name": [
                  "bedouin"
                ],
                "restaurant-pricerange": [
                  "expensive"
                ]
              }
            }
          },
          {
            "actions": [],
            "service": "hotel",
            "slots": [],
            "state": {
              "active_intent": "book_hotel",
              "requested_slots": [],
              "slot_values": {
                "hotel-bookday": [
                  "saturday"
                ],
                "hotel-bookpeople": [
                  "2"
                ],
                "hotel-bookstay": [
                  "2"
                ],
                "hotel-name": [
                  "university arms hotel"
                ],
                "hotel-pricerange": [
                  "expensive"
                ],
                "hotel-type": [
                  "hotel"
                ]
              }
            }
          }
        ],
        "speaker": "USER",
        "turn_id": "8",
        "utterance": "i want to book it for 2 people and 2 nights starting from saturday."
      },
      {
        "frames": [],
        "speaker": "SYSTEM",
        "turn_id": "9",
        "utterance": "Your booking was successful. Your reference number is FRGZWQL2 . May I help you further?"
      },
      {
        "frames": [
          {
            "actions": [],
            "service": "restaurant",
            "slots": [],
            "state": {
              "active_intent": "NONE",
              "requested_slots": [],
              "slot_values": {
                "restaurant-area": [
                  "centre"
                ],
                "restaurant-name": [
                  "bedouin"
                ],
                "restaurant-pricerange": [
                  "expensive"
                ]
              }
            }
          },
          {
            "actions": [],
            "service": "hotel",
            "slots": [],
            "state": {
              "active_intent": "NONE",
              "requested_slots": [],
              "slot_values": {
                "hotel-bookday": [
                  "saturday"
                ],
                "hotel-bookpeople": [
                  "2"
                ],
                "hotel-bookstay": [
                  "2"
                ],
                "hotel-name": [
                  "university arms hotel"
                ],
                "hotel-pricerange": [
                  "expensive"
                ],
                "hotel-type": [
                  "hotel"
                ]
              }
            }
          }
        ],
        "speaker": "USER",
        "turn_id": "10",
        "utterance": "That is all I need to know. Thanks, good bye."
      },
      {
        "frames": [],
        "speaker": "SYSTEM",
        "turn_id": "11",
        "utterance": "Thank you so much for Cambridge TownInfo centre. Have a great day!"
      }
    ]
  }
```


```
{
  "$dialogue_id": [
    "$turn_id": {
      "dialogue_acts": {
        "$act_name": [
          [
            "$slot_name",
            "$action_value"
          ]
        ]
      },
      "span_info": [
        [
          "$act_name"
          "$slot_name",
          "$action_value"
          "$start_charater_index",
          "$exclusive_end_character_index"
        ]
      ]
    }
  ]
}
```

## Model
### Multi-Task Pre-Training for Plug-and-Play Task-Oriented Dialogue System
- [Paper](https://arxiv.org/pdf/2109.14739.pdf)
- [Github](https://github.com/awslabs/pptod)

#### 文章內容摘要
- Task-oriented dialogue is often decomposed into three sub-tasks: 
    - dialogue state tracking (DST)：tracking user’s belief state
    - dialogue policy learning (POL)：deciding which system action to take
    - natural language generation (NLG)：generating dialogue response
- propose a dialogue multi-task pre-training strategy that initialized with T5, pre-train model on a heterogeneous set of dialog corpora that consist of partially-annotated data
- datasets are partially annotated for some of TOD-related tasks, including natural language understanding (NLU), dialogue state tracking (DST), dialogue policy learn- ing (POL), and natural language generation (NLG)

#### 讀後整理
- 目的：在T5上面, 利用大量的部份標註TOD語料訓練1個TOD預訓練模型，後續只需利用少量專業領域語料即可訓練符合專業領域需求的TOD子任務模型
- 作法：利用公開收集且整理過的11個人工標註語料，對T5進行預訓練，並將此做為TOD預測練模型。訓練任務包括各種TOD子任務，包括：NLU, DST, POL, NLG。後續可在此TOD預訓練模型上面用少量數據訓練任何TOD子任務。例如：論文就利用少量的銀行客服數據，訓練1個可以判別用戶意圖的模型(input:用戶查詢,output:想要使用的銀行服務)
- TOD預訓練數據：
    - 2.3M utterances across over 80 domains
    - 各種TOD子任務的標註數據

- 優點：
    - 只要有標註到1個TOD子任務即可做為預訓練數據
    - 可以用來做各種TOD子任務的Few-Shot Training

- 特點：提出「dialogue multi-task pre-training strategy」讓模型可以吃各種部份標註語料及做各種TOD子任務的Few-Shot Training

---
### Multi-Task Pre-Training for Plug-and-Play Task-Oriented Dialogue System
- [Paper](https://arxiv.org/pdf/2111.14592.pdf)
- [Github](https://github.com/siat-nlp/GALAXY)

#### 文章內容摘要
- inject the knowledge of dialog policy explicitly into pre-training 
- build a unified DA taxonomy for TOD and examine eight existing datasets to develop a new labeled dataset named UniDA with a total of 975K utterances
- collect and process a large-scale unlabeled dialog corpus called UnDial with 35M utterances
- propose a semi-supervised pre-training paradigm that applies consistency regularization on all data. It minimizes the bi-directional KL-divergence between model predictions made on dropout-perturbed samples, which facilitates better representation learning from unlabeled dialog corpora
- add a learnable control gate on the KL loss of unlabeled data, so that only good samples are allowed for the consistent regularization, other samples are restricted back to normal self-supervised objectives

#### 讀後整理
- 目的：在UniLM上面, 利用大量未標註TOD語料及少量標註了DA(dialogue action)標籤語料，訓練1個TOD預訓練模型，後續只需利用少量專業領域語料即可finetune符合專業領域需求的TOD end_to_end 任務
- 作法：
    -  將以下4個資訊向量化做為模型輸入：tokens, roles, turns, and positions
    -  預訓練模型同時訓練4個任務：Response Selection,Response Generation,DA Prediction,Consistency Regularization
    -  利用專業領域語料進行finetune
- 特點：提出「with dialogue act annotations as an auxiliary objective」，同時利用DA預測訓練提高預訓練模型的能力

---

### DiactTOD: Learning Generalizable Latent Dialogue Acts for Controllable Task-Oriented Dialogue Systems
- [Paper](https://arxiv.org/pdf/2308.00878.pdf)

#### 文章內容摘要
![截圖 2024-02-25 下午9.32.48](https://hackmd.io/_uploads/SkAlMTd3a.png)

---

### DiagGPT: An LLM-based Chatbot with Automatic Topic Management for Task-Oriented Dialogue
- [Paper](https://arxiv.org/pdf/2308.08043.pdf)
- [Github](https://github.com/windszzlang/DiagGPT/tree/main)

#### 文章內容摘要
- DiagGPT is a multi-agent and collaborative system composed of several modules: Chat Agent, Topic Manager, Topic Enricher, and Context Manager. 
- Each module is a LLM with specific prompts that guide their function and responsibility. Among these modules, the Topic Manager is particularly important as it tracks the dialogue state and automatically manages the dialogue topic
![截圖 2024-02-26 下午1.41.25](https://hackmd.io/_uploads/rJ6oNjFh6.png)

---
### (優先)Guiding Large Language Models via Directional Stimulus Prompting
- [Paper](https://arxiv.org/pdf/2302.11520.pdf)
- [Github](https://github.com/Leezekun/Directional-Stimulus-Prompting/tree/main)

#### 文章內容摘要
- employs a small tunable policy model (e.g., T5) to generate an auxiliary directional stimulus prompt for each input instance. These directional stimulus prompts act as hints and clues to guide LLMs
- the policy model can be optimized through 1) supervised fine-tuning using labeled data and 2) reinforcement learning from offline or online rewards based on the LLM’s output
![截圖 2024-02-26 下午5.00.37](https://hackmd.io/_uploads/BJCL7AY3p.png)

---

## performance metrics
- Inform rate：是否有抓到正確的「實體」。例如：畫新圖,修改圖
- Success rate：是否有抓到正確的「屬性」。例如：正確解出keywrod json 或正確update keyword json

