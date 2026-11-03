AI used = ChatGPT
Conversation share link = https://chatgpt.com/share/6ae9fdb6-ac00-83ea-8b47-57836f6fba3a

Q1: Please review this 'runbook' that was provided to me for my AWS class as homework. Breakdown each part with an explanation of what it is doing, the importance of it, what I am to learn from doing it, and anything else that may be helpful for me to understansd.

AI's answer, in my own words:
I asked AI to evaluate the entire runbook and break it down for me including what I should learn, pay attention to and what concepts apply to real experience. The first thing I noticed was the diagram it created showing the architecture. I had not though of this before of how the code is established in the system our how it should be logically though about.
How I checked it:
I did additional research on it and how I can begin to think like this on a regular basis. 

![[mermaid-diagram.png]]

Q2: What are the commands being used and explanation of them?
AI's answer, in my own words:
AI explained each command what what it should do, I found this very useful as a future reference as the format of the commands often have options I don't know about and show that utilizing the options can save you time. I don't think we'll learn every one and it tells me I need to be conscious of them existing and I should look in to them whenever I run commands. 

AI's answer, in my own words:
I updated my obsidian notes where I have some commands, did some additional research, and re-read the lab.

Q3: What more can you tell me about the installer script?
AI's answer, in my own words:
It broke down what a shell script is, how beneficial it is to use it as opposed to running each command individually, and what the script was doing. It also told me about GnuCOBOL which I never heard of before, I am aware of compilers for coders and learned it is an open source COBOL compiler and allows you to compile and execute COBOL programs on Linux. It also went into what a Python virtual environment was, it allows the applications to maintain separate package instructions which reduces the risk of dependency conflicts. I did some additional research on virtual environments and how scripts work. 

Q4: What is happening when the COBOL program is executed?
AI's answer, in my own words:
It is executing the COBOL program named account lookup. Legacy apps can be composed of independent programs and that COBOL is a human readable code. It then went into the return codes which indicate success or failure. It is important that a system provides this so we know if it is working as expected or not. I re-read the lab and the homework regarding the error codes and how we had to make changes and additions to it. 

Q5: Tell me more about how the web API was started.
AI's answer, in my own words:
It told me that FastAPI is a Python framework for building web APIs. It lets the developer create endpoints that accepts requests and returns responses. Uvicorn is the server that runs the FastAPI application, Uvicorn is the server that runs the app and FastAPI defines the app. Uvicorn serves that applicatino over HTTP. I re-read the lab and did additional research on the break down of it (below). 

|Part|Meaning|
|---|---|
|`uvicorn`|Start the Uvicorn server|
|`app.main`|Import the Python module `main` from the `app` package|
|`:app`|Use the application object named `app`|
|`--host 0.0.0.0`|Listen on all network interfaces|
|`--port 8000`|Listen on TCP port 8000|
