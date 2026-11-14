# Brainees

Brainees is a research reading group.

## Our question for 2026–27

> **Why do neural networks generalize?**

Classical theory says that a model with many more parameters than training examples memorizes the data. Then it fails on new data. But modern neural networks do not fail in this way. Nobody can fully explain why.

This year, we read papers that try to answer this question. We also read papers that show where neural networks fail. These failures help us test the answers.

## What is in this repository

| Item | Content |
|---|---|
| [`sessions/`](sessions/) | One folder for each session: notes, questions and answers, and the paper (if it is open access). |
| [`knowledge-tree.md`](knowledge-tree.md) | One diagram that shows how the papers connect to our question. |

## How a session works

1. We will choose a paper and two **session leads**.
2. The session leads open an issue with the **Session** template. The issue gives the paper, the pages to read, and the date.
3. All members read the paper before the session.
4. All members write a comment on the issue: one question and one claim that they doubt.
5. In the session, the two session leads present the paper. Then we discuss it together.
6. After the session, the session leads make a pull request. The pull request adds:
   - a session folder, made from [`sessions/TEMPLATE.md`](sessions/TEMPLATE.md)
   - a node for the paper in [`knowledge-tree.md`](knowledge-tree.md)
7. Each member adds their own notes as one file in the session folder, for example `sessions/Session_1/Bilal_SESSION_1_notes.md`. Then they make a pull request.

## How to add something 

1. Go to the file or folder on github.com.
2. To make a new file, click **Add file**. To change a file, click the pencil icon.
3. Make your change.
4. Click **Commit changes**. Select **Create a new branch**. Click **Propose changes**.
5. Click **Create pull request**.
6. A group lead reviews the pull request and merges it.

## Session folders

- Each session has one folder: `sessions/Session_1/`, `sessions/Session_2/`, and so on.
- `README.md` is the main file. It has the paper title, the link, the session leads, and the questions and answers. Make it from [`sessions/TEMPLATE.md`](sessions/TEMPLATE.md). GitHub shows this file when you open the folder.
- Each member adds one notes file: `<YourName>_SESSION_<N>_notes.md` (or `.txt`). Example: `Bilal_SESSION_1_notes.md`. One file for each person, so pull requests do not conflict.
- You can add photos or figures to the same folder.

## Replications

Replications are optional. For some papers, the group can decide to replicate a result. Put the code in `replication/<YourName>/` in that session's folder.

