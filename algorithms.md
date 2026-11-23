# Algorithmic Approach

This document records the intended algorithmic techniques for SkillBridge. Mark each technique as implemented only after it exists in the source code and is covered by suitable tests.

## 1. Skill matching

A candidate's extracted skills can be compared with the skills associated with a selected role. A weighted score can account for the relative importance of each required skill.

Document the final scoring formula, normalization method, and treatment of synonyms here once implemented.

## 2. Text representation and similarity

TF-IDF can represent resume and role-description text as numerical vectors. Cosine similarity can compare those vectors:

\[
\operatorname{similarity}(A,B)=
\frac{A\cdot B}{\|A\|\|B\|}
\]

Text similarity should supplement structured skill matching rather than being presented as a definitive measure of employability.

## 3. Skill dependency graph

Represent prerequisite relationships as a directed graph. For example, a foundational programming skill may be a prerequisite for data structures, which may precede advanced algorithms.

Document the graph representation, edge meaning, and cycle-handling strategy after implementation.

## 4. Shortest-path learning sequence

Dijkstra's algorithm is suitable only when graph edge weights are non-negative and the chosen path objective is meaningful. Define what an edge cost represents (for example, estimated learning effort) before interpreting the result as an optimal learning path.

## 5. Priority-based skill ranking

A priority queue can order missing skills using a documented priority score, such as role importance and prerequisite readiness.

## Testing expectations

For each implemented algorithm, include:
- Input and output definitions.
- Time and space complexity.
- Edge cases.
- Unit tests.
- A short explanation of how the algorithm is integrated into the application.
