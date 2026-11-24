# Ariadne — A Companion for Exploratory Philosophical Learning

*A Thread Through Philosophy*

**A thread through the labyrinth of philosophy.**

Ariadne is an AI learning workflow for reading primary philosophical texts, understanding concepts, and exploring questions. It aims to help learners begin with philosophical works, gradually understand a philosopher’s thought, develop questions of their own, and lay a foundation for later research and academic writing.

In Greek mythology, Ariadne gave Theseus a thread so that he could find his way back through the labyrinth.

The name expresses the idea behind the project: **AI can offer threads and guidance for philosophical exploration, but it is the learner who enters the text, develops an understanding, and thinks.**

Rather than primarily producing quick summaries of philosophical knowledge, Ariadne tries to make AI a reading tutor that can adapt its teaching to the learner’s particular situation.

> **Let AI help you understand philosophy, not do your philosophical thinking for you.**

**Current version:** v1.0.0

**Project status:** Its educational effectiveness has not been systematically validated across users. See the [MIT License](LICENSE).

[中文](README.md) · [Installation](INSTALL.md) · [Changelog](CHANGELOG.md)

## 1. Why develop Ariadne?

Philosophical learning differs from learning facts in an important way:

**Knowing what view a philosopher held is not the same as understanding it.**

For example, it is easy to get an AI to answer:

- Kant held that space and time are a priori forms of sensibility.
- Heidegger held that the animal is poor in world.
- Deleuze held that becoming is neither imitation nor a change of identity.

But these answers do not in themselves ensure that we understand the philosophical problems involved.

Understanding also calls for further questions:

- Why does a philosopher introduce a concept?
- What problem are they trying to address?
- How do they develop their thought through arguments, descriptions, or examples in their texts?
- How does one concept relate to others?
- Is the account adequate, and how might we question it?

These questions can be difficult for independent readers. We may lack the background needed to enter a text, or understand the literal meaning of every sentence while still failing to grasp the significance of the passage as a whole.

General-purpose AI can already offer many philosophical explanations. In a typical question-and-answer exchange, however, the user must still decide what to ask or read next, and how to judge whether they have really understood.

Ariadne takes up a further question:

**Can AI do more than answer philosophical questions? Can it continually organize and adjust its teaching around a learner’s actual process of understanding?**

This means attending not only to what a text says, but also to what the learner understands, what remains unclear, and which next step would actually help.

## 2. What can Ariadne do?

### 2.1 Organize reading around your philosophical interests

You do not need a complete reading plan before you begin.

For example, you might start with:

> I want to understand how Heidegger thinks about animals and their relation to the world. I have read some of *Being and Time*, but I have not systematically studied his account of animality.

Ariadne can help you:

- clarify the philosophical question you currently want to understand;
- look for relevant primary texts and important passages;
- explain why those texts may be useful starting points;
- suggest a reading sequence in light of your existing knowledge; and
- adjust the route as your reading develops.

It does not require every learning project to begin with a fixed research question.

If you only want to understand a short passage you have encountered, you can begin there without first setting up a complete research project.

### 2.2 Help you read and understand primary texts

Ariadne treats primary texts as a central basis for developing and calibrating understanding.

In working with a text, it can help you:

- follow the development of an argument;
- understand a concept’s role in its context;
- analyze the examples a philosopher uses;
- connect passages elsewhere in the same work;
- explain relevant historical or theoretical background; and
- identify points the text has not adequately explained.

It does not assume that all philosophical texts should be read in the same way.

For example, reading an argument by Descartes, a phenomenological description by Merleau-Ponty, and Deleuze’s experimental conceptual writing may call for different teaching strategies.

Sometimes understanding an argument requires reconstructing its premises and reasoning. Sometimes understanding a phenomenological concept calls for close attention to descriptions of experience. In other cases, understanding a concept may require connecting chapters of the same work or examining knowledge the author draws from another discipline.

Ariadne tries to choose an approach in response to the text rather than follow one fixed sequence for every case.

### 2.3 Adapt its explanations to your difficulty

When you say you do not understand, Ariadne should do more than repeat the same conclusion in different words.

It tries to identify where the difficulty lies. For example:

- You do not recognize a term.
- You understand its definition but not why the concept is needed.
- You can restate two claims but do not see their connection.
- You lack the empirical knowledge needed to understand an example in the text.
- You understand the author’s account but think its reasons are inadequate.

Different difficulties may call for different responses: background, another passage, a guide, analysis of an example, a provisional explanatory model, or a joint examination of an argument.

For example, if you do not understand why Deleuze calls the relation between orchid and wasp a “becoming,” repeating that “becoming is not imitation but an alliance between heterogeneous beings” may not resolve the difficulty.

What may need explaining is: **Why can this relation be understood as an actual becoming rather than simply an ordinary interaction between two species?**

Ariadne should try to recognize such a difficulty and adjust its explanation accordingly. These methods are not a fixed sequence that must be followed in order.

### 2.4 Help you develop independent philosophical understanding

Ariadne is concerned not only with whether it has given a plausible explanation, but also with whether you have understood.

It might invite you to:

- explain a concept in your own words;
- explain why an author’s argument needs a premise;
- analyze how an example illustrates a conceptual relation;
- raise an objection to an account; or
- return to the text to check an interpretation.

But Ariadne should not turn every exchange into a recall test.

**Repeating an AI’s answer is not the same as having formed an independent philosophical understanding.**

A learner may grasp an author’s basic claim without yet understanding its argument. Or they may understand why the author says something and then find a point worth questioning.

Once you have developed a reasonable understanding, or when the current difficulty has become a question worth investigating further, Ariadne may suggest continuing the reading, taking stock of what has been learned, or leaving the question open for now.

Progress in philosophy does not always mean that a question has been finally resolved. Sometimes it means that the learner can at last ask a more precise and more searching question.

### 2.5 Let questions change through reading

Exploratory learning does not mean always looking for an answer to the question with which you began.

In reading primary texts, you may gradually discover that your initial question was not well framed. This need not simply reflect a lack of knowledge: the question itself may contain an unnoticed philosophical assumption. As understanding deepens, that assumption may be challenged and the question may need to be reformulated.

For example, you might initially turn to Kant’s *Critique of Pure Reason* with the question:

> How does the subject’s knowledge conform to an objective object that exists independently of the subject?

This might carry a particular epistemological assumption: that the object, as an object of knowledge, already has a determinate structure, and that the task of knowledge is to explain how the subject obtains representations that conform to it.

As you read Kant, however, you may find that he seeks to change this traditional way of framing the problem. Instead of simply assuming that knowledge must conform to objects, he asks us to consider whether objects, as objects of possible experience, must instead conform to the subject’s a priori conditions of cognition.

As your understanding develops, the original question may no longer adequately express the problem Kant is trying to address. Rather than continuing in the same direction, you might reformulate it:

> How do the subject’s a priori conditions of cognition make experience of objects possible? Why does Kant think we must reconsider the relation between knowledge and objects in this way?

Here, reading has helped the learner discover a theoretical assumption in the original question and change the question itself.

Ariadne tries to help learners discover, examine, and revise such assumptions as they read, and to adjust subsequent learning goals and reading paths accordingly.

This does not mean that AI may decide on the learner’s behalf which question is correct. The revision should arise from the learner’s deepening engagement with the text; Ariadne’s role is to offer guidance and support.

### 2.6 Support sustained learning

Ariadne can be used for a single reading discussion or for sustained philosophical learning.

With an appropriate host and project configuration, it can help you:

- maintain a coherent reading path;
- record what you have read and understood;
- retain unresolved philosophical questions;
- track significant textual locations and literature leads; and
- organize conceptual understandings worth preserving.

This can make it unnecessary to explain the entire learning background in every exchange.

The extent of these functions depends on the AI agent, file-access tools, and project configuration. Ariadne’s basic learning functions do not require an existing personal corpus, note system, or research project. Nor does it treat every discussion as an event that must produce a note or update project state.

## 3. How do Ariadne, general-purpose AI, and independent reading differ?

| Dimension | Independent reading | General-purpose AI | Ariadne |
| --- | --- | --- | --- |
| Core approach | The learner reads, thinks, and checks sources | Generates answers to the user’s questions | Organizes teaching around the process of understanding |
| Entry into reading | Chosen by the learner | Usually specified by the user | Can suggest an entry based on goals and readiness |
| Difficulties | The learner looks for ways forward | Usually offers an explanation | Tries to diagnose the difficulty and adapt its approach |
| Primary-text evidence | Managed by the reader | Depends on the model and prompt | Treats primary texts as an important basis for calibration |
| Continuity | Relies on personal notes | Relies mainly on conversation and platform capabilities | Can be used with persistent project records |
| Exploring questions | Driven by the learner | Driven mainly by user questions | Tries to help discover and deepen questions |

**Ariadne is not a more powerful foundation model than general-purpose AI.**

It is a specialized learning method and workflow built on top of a model, intended to encourage more consistent and targeted teaching behavior in philosophy. Put simply, general-purpose AI mainly responds to your present question; Ariadne tries to organize such answers into a developing learning process.

The difference is not absolute. Given suitable prompts, relevant primary texts, and a continuing conversation, general-purpose AI can perform many of the same tasks. Ariadne’s intended advantage is to reduce the burden of repeatedly designing prompts, finding entry points, and adjusting teaching methods—not to guarantee that it is always better.

Nor can Ariadne replace independent reading. One of its goals is precisely to help learners improve their ability to understand primary texts independently.

## 4. How do I get started?

Ariadne is a learning workflow for an AI agent that supports Skills, not an independent foundation model. Initial installation requires an appropriate environment. See the [installation guide](INSTALL.md) for setup, verified platforms, and limitations.

**Once installed, using Ariadne does not require programming, prompt engineering, or knowledge of an AI agent’s internals.**

Prepare:

1. **A philosophical interest or question:** it can be specific or simply concern a philosopher you want to understand.
2. **Your existing knowledge:** briefly say what you have read and what you know.
3. **Your goal:** for example, understanding a concept, reading a chapter, or exploring a philosophical question.

If you have an electronic copy of a text, you can provide it when the host supports that. If not, you can ask for help finding suitable material. You may begin a sustained learning project or go directly to a difficulty in your current reading.

### Example 1: Begin an exploratory learning project

> I want to understand Spinoza’s account of natural right. I have read part of the *Ethics* and know that conatus concerns an individual’s power to persist, but I have not read his political works.
>
> I want to read the relevant primary texts to understand why Spinoza connects natural right with power.
>
> Please help me begin using the exploratory learning workflow.

Ariadne should first consider an appropriate entry in light of your goal and readiness, rather than immediately provide a complete summary of the theory.

### Example 2: Raise a difficulty

> I understand the connection Spinoza draws between natural right and power, but I do not understand this: if right depends on power, what independent significance do law and justice have in a political community?

Ariadne should try to address the conceptual difficulty directly and consult relevant texts or explanatory resources as needed.

### Example 3: Offer a criticism

> I understand the author’s account, but I do not think the reasons are sufficient. Can we examine how strong a conclusion the argument actually supports?

Ariadne should not presume that the philosopher must be right or automatically treat the learner’s criticism as a misreading.

## 5. Recommended ways to use Ariadne

Ariadne is best suited to sustained philosophical exploration centered on primary texts, rather than use as an encyclopedia that answers unlimited questions.

In practice:

- **Read primary texts yourself when possible.** Do not rely only on AI summaries.
- **Describe difficulties honestly.** You do not need to give an answer that merely looks correct.
- **Question the AI.** If an explanation remains unclear, say what is missing.
- **Distinguish an author’s view from the AI’s interpretation.** A useful model need not be the author’s explicit argument.
- **Keep worthwhile new questions.** Not every issue has to be resolved in the same discussion.

You can also say:

> Please do not give me the conclusion yet; I want to try understanding the passage myself.

Or:

> My difficulty is not the wording of the text. I do not see why the concept is necessary.

Or:

> Your explanation seems to repeat the author’s concepts without answering my question.

Feedback like this can help Ariadne adjust its approach.

You do not need to treat it as an infallible teacher. It is better understood as a learning partner whose contributions can be discussed, criticized, and revised, while you retain your own judgment about the text.

## 6. Limitations

Ariadne remains an experimental philosophical learning workflow, not a rigorously validated teaching system.

**AI can still make mistakes.** It may misread a learner, misunderstand a text, confuse translations, provide unverified quotations, or give inaccurate background. Check important quotations, locations, and scholarly judgments yourself.

**A plausible explanation is not necessarily a rigorous argument.** Ariadne may use provisional explanatory models, but they must be tested against the text and cannot automatically be treated as the author’s explicit reasoning.

**It may not know how much you understand.** Repeating its explanation does not by itself show independent mastery.

**Teaching strategies may not always work.** It may over-explain, ask too many questions, or misidentify the difficulty. You can ask it to change its approach.

**Sustained learning depends on the host.** Project records, access to texts, retrieval, and notes depend on the platform, tools, and permissions available.

**Models may perform differently.** Ariadne guides an AI’s organization of learning; its actual performance also depends on the model and environment.

It should not replace reading the texts, checking scholarship, guidance from philosophy teachers, or the learner’s own judgment.

## 7. Questions the project is exploring

Ariadne focuses on three areas.

### Adaptive philosophical teaching

Can AI choose appropriate strategies in light of the learning goal, the character of the text, and the learner’s understanding? This involves not only offering different explanations, but judging when to explain further, return to the text, or leave space for independent thinking.

### Textual understanding and independent thought

How can we tell whether a learner has developed an understanding grounded in the text rather than merely accepted or repeated the AI’s answer? Understanding requires fidelity to the text as well as grasping conceptual relations, reasons, and possible weaknesses.

### Open-ended philosophical exploration

Can AI help learners discover, deepen, and adjust questions through reading instead of mechanically completing a preset plan? A new question need not mean the original goal has failed; it may show that understanding is deepening.

These questions remain open and guide the project’s continuing tests.

## 8. Trying Ariadne and giving feedback

Ariadne welcomes exploratory feedback from people interested in reading philosophical texts. You do not need to know its technical design. Choose a question that genuinely interests you and that you do not yet fully understand.

After trying it, useful feedback includes:

- Which explanation actually helped you understand the text?
- Did Ariadne identify your difficulty accurately?
- Did it over-explain, repeat questions, or interrupt your reading?
- Did it help you form a new philosophical question?
- How did the experience compare with independent reading or general-purpose AI?

Reports of incorrect quotations, unsuitable reading paths, installation difficulties, and other problems are also welcome. Such feedback can help assess whether Ariadne supports philosophical understanding rather than merely generating more elaborate teaching conversations.

For installation, current test status, and feedback channels, refer to the repository documentation when the project is formally released.

## 9. About the project

Ariadne is an AI workflow experiment built around primary-text reading and exploratory philosophical learning.

Its long-term goal is not to create a system that replaces the judgment of philosophy teachers or researchers, but to explore:

**Can artificial intelligence become a genuinely helpful tool for philosophical understanding, independent reading, and the formation of questions?**

The project was initiated and developed by Muxiang Yan, with assistance from ChatGPT and other AI tools in design, testing, and documentation.

Ariadne runs in an AI agent environment that supports Skills. Installation requirements and compatibility for any public version are described in its release documentation. The project remains under development and testing; discussion, trials, and improvements from philosophy learners are welcome.

*Ariadne — A Thread Through Philosophy.*

**Ariadne provides the thread, but it is the learner who enters the labyrinth.**
