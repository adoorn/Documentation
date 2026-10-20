# Analyze Error(s)

## Occasional system errors may occur within the software. In this section, you will learn how to determine the cause and apply the appropriate solution

> [!TIP] Use a search engine or AI tool

A common tip from IT experts: make use of search engines or AI assistants such as Copilot or ChatGPT. When you look up standard Dynamics functionalities, there's a good chance you'll quickly find the answer to your question.

### We can separate system errors into two main categories

1. Webclient Errors
2. App Platform errors

#### 1. Webclient Errors

If you encounter an error message like the one shown below, you will mainly see two elements: the Error Message itself, and the option to Copy or Share the Callstack.
You can copy the callstack to view more details about the error, such as which status or step function is causing it. Understanding this information may help you resolve the issue yourself or provide more precise details to the Support team — resulting in faster resolution and increased system uptime.

![1](../1.png)

If you open the callstack, you will mainly see two elements: the Error Message itself and the Function Name. Knowing this, you can identify which function is causing the error. You can then either acknowledge that this function triggers the error or review the specific function to make the necessary changes.

![2](../2.png)

![4](../4.png)

> [!Note] For more information about status templates and step functions, have a look at pages:
>
> - [Status Templates](StatusTemplates.md)
> - [Steps](Steps.md)

If you want to know which error occurred last in the system, go to the "Latest Error" page via Tell Me. This page shows the most recent error details, including the error message and the callstack.

![3](../3.png)

If you want to know which error occurred in the Job Queue, go to the "Job Queue Entries" page via Tell Me. Here, you can view all job queues. Open the Log Entries for the relevant job.

![11](../11.png)

Then select View Callstack to see the callstack details. If the issue is clear and you can resolve it yourself, go ahead. If not, contact Support for assistance.

![10](../10.png)

Sometimes, an error may occur without executing a status or step — for example, when filling in a field. In the example below, an error occurred while entering an existing address in the Ship-to field. By clicking the red error icon next to the value you entered, you can view more details about the error. From there, you can choose to copy or share the error message for further analysis or to provide to Support.

![8](../8.png)

When checking this address, we see that the Ship-to boolean is set to False, which means the address is not marked as a ship-to address. By changing this value to True, you can proceed with the receipt process.

![12](../12.png)

#### 2. App Platform errors
<!--  -->

When an error occurs in the scanner and you don’t immediately know the cause, you can go to Scan Sessions (which store data during the scanning process) to investigate the issue. In the scan session, you can view your session variables and download or open the Callstack to get more details about the problem.

![5](../5.png)

![6](../6.png)

When opening the callstack, you can find the most recent scan session variables, the callstack details, and the specific function that caused the error message. Now you know the source of the error (in this example, Function 11 is the cause). From here, you can decide whether this is expected behavior or if it requires further attention.


![7](../7.png)

> [!Note] If you want to learn more about scanning, check out the page [Scanning Application Documentation](Scanning.md)

> [!TIP]
> Are the actions functionally correct?

> -You know better than anyone how the system works and what it is designed to handle. If you discover that one of your actions triggers unexpected results or values that the system is not designed to process, it can be helpful to ask a colleague to take a second look. Sometimes, two sets of eyes can spot something you might have missed.

> -To avoid affecting your production environment, perform a “trial and error” test in the reporting environment to narrow down the issue.
>For example, ask yourself: “Does the result change if I modify a value on the header or line of the document, or enable/disable a function during the status transition?”

> If the problem also occurs in the copy data from yesterday, and it is not related to printing, mailing, or data integration, you are free to adjust the conditions. This helps determine whether the issue is caused by user input or by the software itself.

> -Are you using an external application? Sometimes, problems originate outside Dynamics.
