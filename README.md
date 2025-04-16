# Intent-Analysis


## Problem 1 : Case Study: Hotel Booking Chatbot

### Part A: Multilingual Intent Detection

The model used for Intent Detection is `nomic-ai/nomic-embed-text-v1`, which is a lightweight model. This analysis shows that lightweight LLMs have the capability to tackle complex classification tasks. Since we require a hotel management chatbot, there should be a limited number of responses. Just like zomato chatbot, the conversations should only include specific intents, and not a truly general chatbot.

The intent list has been extended to 

```bash
[
    "book_room",
    "cancel_booking",
    "request_special_offer",
    "ask_about_local_attractions",
    "resolve_complaint",
    "check_availability",
    "inquire_room_rate",
    "modify_booking",
    "extend_booking",
    "request_late_checkout",
    "ask_wifi_availability",
    "request_room_service_menu",
    "ask_pet_policy",
    "ask_parking",
    "request_wakeup_call",
    "request_extra_bed",
    "ask_airport_pickup",
    "request_manager",
    "request_room_preference",
    "cancel_breakfast",
    "ask_gym_spa",
    "request_quiet_room",
    "preorder_meal",
    "ask_checkin_policy",
    "ask_checkout_policy",
]
```

The categorization works pretty well.


### Part B: Basic Conversation Patterns Analysis

In this section, we use the same `nomic-ai/nomic-embed-text-v1` to train on some examples. The model does very good in picking out the best response from the limited dataset. As mentioned earlier, we want an LLM which is well-versed in working with only a specific set of queries and responses. If any query that a user has goes beyond the use-case of the chatbot, we can have a direct call feature so that the user's doubts are mitigated. 


## Problem 2: Prompt Engineering

In this problem statement we are required to make a generalized chatbot which can talk to the user in GPT style. Langchain has been used to build a prompting pipeline to talk to the LLM. We are using `gemini-1.5-pro-latest`, which is a high-end LLM. 
Earlier we were using a lightweight LLM, which worked nicely only in certain conditions with some context provided to it. When it comes to tasks like this, gemini and GPT based models take the cake. They can give us good results even with little or no provided context.





## Extra Notes

This project also compares lightweight LLM(`nomic-ai/nomic-embed-text-v1`) and high-end LLM(`gemini-1.5-pro-latest`) and their workings. The lightweight LLMs can given good results under certain conditions and with the right context provided to it. Whereas, the high-end LLMs gives good results even without context.
