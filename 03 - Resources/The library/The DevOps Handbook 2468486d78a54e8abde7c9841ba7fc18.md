# The DevOps Handbook

## 0. The Three ways

## 1. Introduction

Myth—DevOps Replaces Agile: DevOps principles and practices are
compatible with Agile, with many observing that DevOps is a logical
continuation of the Agile journey that started in 2001. Agile often serves
as an effective enabler of DevOps because of its focus on small teams
continually delivering high-quality code to customers.

---

### Opposed goals

Frequently, Development will take responsibility for responding to changes in the market and for deploying features and changes into production as quickly as possible. IT Operations will take responsibility for providing customers with IT service that is stable, reliable, and secure, making it difficult or even impossible for anyone to introduce production changes that could jeopardize production. Configured this way, Development and IT Operations have diametrically opposed goals and incentives.

---

### Every company is a tech-company

First, as described earlier, every IT organization has two opposing goals, and second, every company is a technology company, whether they know it or not. As Christopher Little, a software executive and one of the earliest chroniclers of DevOps, said, “Every company is a technology company, regardless of what business they think they’re in. A bank is just an IT company with a banking license.” To convince ourselves that this is the case, consider that the vast majority of capital projects have some reliance on IT. As the saying goes, “It is virtually impossible to make any business decision that doesn’t result in at least one IT change.”

---

### The cost of bad DevOps processes

When people are trapped in this downward spiral for years, especially those who are downstream of Development, they often feel stuck in a system that preordains failure and leaves them powerless to change the outcomes. This powerlessness is often followed by burnout, with the associated feelings of fatigue, cynicism, and even hopelessness and despair. Many psychologists assert that creating systems that cause feelings of powerlessness is one of the most damaging things we can do to fellow human beings—we deprive other people of their ability to control their own outcomes and even create a culture where people are afraid to do the right thing because of fear of punishment, failure, or jeopardizing their livelihood. This type of culture can create the conditions for learned helplessness, where people become unwilling or unable to act in a way that avoids the same problem in the future. For our employees, it means long hours, working on weekends, and a decreased quality of life, not just for the employee, but for everyone who depends on them, including family and friends. It is not surprising that when this occurs, we lose our best people (except for those who feel like they can’t leave because of a sense of duty or obligation). In addition to the human suffering that comes with the current way of working, the opportunity cost of the value that we could be creating is staggering—the authors believe that we are missing out on approximately $2.6 trillion of value creation per year, which is, at the time of this writing, equivalent to the annual economic output of France, the sixth-largest economy in the world. Consider the following calculation—both IDC and Gartner estimated that in 2011 approximately 5% of the worldwide gross domestic product ($3.1 trillion) was spent on IT (hardware, services, and telecom).10 If we estimate that 50% of that $3.1 trillion was spent on operating costs and maintaining existing systems, and that one-third of that 50% was spent on urgent and unplanned work or rework, approximately $520 billion was wasted. If adopting DevOps could enable us—through better management and increased operational excellence—to halve that waste and redeploy that human potential into something that’s five times the value (a modest proposal), we could create $2.6 trillion of value per year.

---

### Purposely injecting errors - in the name of Quality

Because we care about quality, we even inject faults into our production environment so we can learn how our system fails in a planned manner.

---

### More developers reduce individual productivity

This is highlighted in the famous book by Frederick Brook, the Mythical Man-Month, where he explains that when projects are late, adding more developers not only decreases individual developer productivity but also decreases overall productivity.13

---

### The problems are universal

As with The Goal, there is tremendous evidence of the universality of the problems and solutions described in the Phoenix Project.

## 2. Part I: The three ways

### Fast feedback is achieved by modular architecture

This is most easily achieved when we have architecture that is modular, well encapsulated, and loosely coupled so that small teams are able to work with high degrees of autonomy, with failures being small and contained, and without causing global disruptions. In this scenario, our deployment lead time is measured in minutes, or, in the worst case, hours. Our resulting value stream map should look something like Figure 1.3.

![Untitled](Untitled.png)

---

### Conditions to maximize flow

The First Way enables fast left-to-right ìow of work from Development to Operations to the customer. In order to maximize ìow, we need to make work visible, reduce our batch sizes and intervals of work, build in quality by preventing defects from being passed to downstream work centers, and constantly optimize for global goals.

![Untitled](Untitled%201.png)