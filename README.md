# AI-powered expense tracker
AI Engineering — Topic 1 Lab | 15 of 17
> Take picture of physical and digital receipts to summarize visually and give personalized recommendations.
## Problem Statement
Manual expense tracking is slow and tedious. Additionally, these days our money and transaction are spread across multiple e-wallet apps, difficult to keep track. This mobile app able to solve these problems by automate expense logging in one centralized location.
## Evidence of the Problem
1. Manual expense tracking through spreadsheets or paper creates bottlenecks, especially as companies scale (SoftCo, 2025). Reasons why it’s important to address: (1) Spreadsheets and emails are error-prone and time-consuming. (2) Manual matching and validation delay month-end close.(3) Inconsistent data leads to inaccurate forecasting. 

https://softco.com/blog/7-expense-management-problems-costing-you-time-money/

2. According to The Edge Malaysia (2022), managing expenses has become increasingly complex and inconvenient for the author due to the fragmentation of funds across multiple e-wallets (such as Touch ’n Go, Grab, and 1Pay), physical cards, bank accounts, and emergency cash. Unlike relying on traditional cash, tracking daily spending now requires constant monitoring of various digital balances and physical card top-ups, a burden the author expects will only grow as more retailers launch their own proprietary payment apps. 

https://theedgemalaysia.com/article/comment-challenge-users-multiple-ewallets-face 

## Initial Related Work / Existing Approaches

1. Pawar et al. (2025): Developed a financial assistant that lets users manage their finance through typed commands in natural language. It uses a PHP front end, a Python Flask back end, and a MySQL database. When a user asks “What was my coffee expenditure last month?”Google's Gemini LLM interprets the question and generates output through the SQL query.
Limitations: Reliance on a legacy PHP 5.6 stack, which constrained integration and security, and by difficulty interpreting complex natural-language queries, a challenge that remains open in NLP. 
2. Guru & Subramaniam (2026): Built a personalized, real-time expense categorization system. It uses OCR to extract the merchant, date, and amount from physical and digital receipts, then uses retrieval-augmented generation (RAG) to categorize each expense, drawing on the user’s past spending patterns and preferred categories.
Limitations: Dataset covers mainly English and a few other major languages, and Malay and MYR are not explicitly listed, so its applicability to the Malaysian market is uncertain and would need to be validated on local data. 
3. Lin et al. (2022): Built an automatic receipt recognition system (ARRS) that reads receipts using deep learning. It reports 80.93% accuracy on handwritten characters, and its YOLOv4-s model reached 99.39% accuracy on printed characters, with only 33 characters misjudged.
Limitations:The authors note that ARRS currently runs only on a personal computer, limiting portability, and that its handwritten receipt data and recognition accuracy need improvement. Evaluation also does not yet include formal uncertainty analysis 

## Project Objectives
O1: To investigate the current limitations, performance metrics, and technological requirements of existing expense trackers. 

O2: To develop an AI-powered expense tracker, using Malaysian receipt and QR payment data, that consolidates records from multiple bank and e-wallet apps and provides grounded, personalized insights through retrieval-based question answering.

O3: To evaluate the solution in terms of answer quality, groundedness, latency, and safety.  

## Target Users
Small business owners and digitally active consumers who frequently use mobile banking and e-wallet solutions. 

## Data Sources
ICDAR2019 SROIE: contains 987 receipt images in English, annotated with key fields (company, date, address, and total) and bounding boxes with transcripts for all text regions in the images.

https://huggingface.co/datasets/jsdnrs/ICDAR2019-SROIE 
