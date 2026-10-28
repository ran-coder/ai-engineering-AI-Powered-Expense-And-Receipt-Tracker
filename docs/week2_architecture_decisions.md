

| Decision | Requirement / Constraint | Alternatives Considered | Selected Option | Trade-off Accepted |
| :---- | :---- | :---- | :---- | :---- |
| Manually put the e-wallets receipt | Software integration with bank apps constraints | bank API access  | User upload of payment confirmation screenshots and statement files  | More user effort and no automatic capture, but no credentials collected  |
| Compute totals with SQL, not LLM arithmetic.  | Answers must be factually grounded  | LLM calculates from retrieved text  | SQL computes, LLM only explains.  | extra query-generation step and possible failures on unusual questions, in exchange for correct numbers.  |

| Objective | Requirement | Evaluation Criterion | Architecture Element | Later Evidence |
| :---- | :---- | :---- | :---- | :---- |
| \[O1\] | NFR4 | seamlessness of task completion | Web front end  | pilot test report showing task completion rate and navigation ratings. |
| \[O2\] | NFR2 | numeric accuracy and faithfulness  | SQL query layer  | test results showing numeric accuracy and faithfulness.  |
| \[O3\] | NFR5 | seamlessness of data handoffs | Schema validation at each handoff (OCR, database, LLM)  | pilot test report showing integration test pass rate and value-mismatch rate across all handoffs.  |

