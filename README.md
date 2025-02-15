\documentclass{article}
\usepackage{hyperref}
\usepackage{listings}
\usepackage{xcolor}
\usepackage{graphicx}

\title{Palindrome Checker - Server-Client Application}
\author{}
\date{\today}

\begin{document}

\maketitle

\section{Overview}
This project is a \textbf{server-client palindrome checker} implemented using \textbf{Python} and \textbf{socket programming}. The application consists of a \textbf{server} that processes palindrome requests and a \textbf{client} with a \textbf{Graphical User Interface (GUI)} for user interaction.

The program supports:
\begin{itemize}
    \item \textbf{Simple Palindrome Check}: Determines if a given string is a palindrome while ignoring spaces, punctuation, and case sensitivity.
    \item \textbf{Complex Palindrome Check}: Determines if a string can be rearranged to form a palindrome and calculates the minimum number of swaps required.
\end{itemize}

\section{Assignment Objective}
The goal of this assignment is to develop a \textbf{concurrent server-client application} using \textbf{socket programming} that performs palindrome checking and allows multiple clients to connect simultaneously.

\textbf{Key Features:}
\begin{itemize}
    \item Multithreaded TCP Server to handle multiple client requests.
    \item Logging Mechanism to track client requests and responses.
    \item GUI Client using Tkinter for an interactive user experience.
    \item Timeout Handling: The client retries if the server does not respond within a given timeframe.
    \item Two modes of palindrome checking (simple and complex).
\end{itemize}

\section{Project Structure}
\begin{verbatim}
├── server.py         # The server-side code handling palindrome checks
├── client.py         # The command-line based client (alternative to GUI)
├── gui.py            # The Tkinter-based GUI client
├── README.md         # This file containing project details
├── server_log.txt    # Log file recording client requests
\end{verbatim}

\section{Installation and Execution}
\subsection{Prerequisites}
\begin{itemize}
    \item Python 3.x
\end{itemize}

\subsection{Steps to Run the Program}
\subsubsection{1. Start the Server}
\begin{lstlisting}
python server.py
\end{lstlisting}
This will start the TCP server, listening for client connections.

\subsubsection{2. Run the GUI Client}
\begin{lstlisting}
python gui.py
\end{lstlisting}
This will launch the graphical user interface where you can input a string and check for palindromes.

\section{How It Works}
\subsection{Server}
\begin{enumerate}
    \item Receives client requests over a TCP connection.
    \item Processes the request to check for palindrome properties.
    \item Logs client interactions into \texttt{server_log.txt}.
    \item Responds to the client with the palindrome check results.
\end{enumerate}

\subsection{Client (GUI)}
\begin{enumerate}
    \item User inputs a string into the text box.
    \item Selects Simple or Complex Palindrome Check using radio buttons.
    \item Clicks 'Check', which sends the request to the server.
    \item Receives and displays results in a message box.
\end{enumerate}

\section{Example Usage}
\subsection{Simple Palindrome Check}
\textbf{Input:}
\begin{verbatim}
A man, a plan, a canal, Panama
\end{verbatim}
\textbf{Processed as:}
\begin{verbatim}
amanaplanacanalpanama
\end{verbatim}
\textbf{Output:}
\begin{verbatim}
Palindrome: True
\end{verbatim}

\subsection{Complex Palindrome Check}
\textbf{Input:}
\begin{verbatim}
ivicc
\end{verbatim}
\textbf{Output:}
\begin{verbatim}
Palindrome: True
Swaps Needed: 2
\end{verbatim}

\section{Additional Features}
\begin{itemize}
    \item \textbf{Logging}: The server logs each request with the client’s IP address, request type, input string, and result.
    \item \textbf{Timeout Handling}: The client will retry the request up to 3 times if the server does not respond.
    \item \textbf{GUI Enhancements}: A user-friendly graphical interface for ease of use.
\end{itemize}

\section{Conclusion}
This project successfully implements a \textbf{networked palindrome checker} using Python's socket programming and Tkinter for the client GUI. The program handles \textbf{multiple clients}, maintains logs, and processes \textbf{both simple and complex palindrome checks} efficiently.

\end{document}
