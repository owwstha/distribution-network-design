#distribution-line-design
\documentclass[11pt, a4paper]{article}
\usepackage[a4paper, margin=2.5cm]{geometry}
\usepackage{fontspec}
\usepackage[english, bidi=basic, provide=*]{babel}
\babelprovide[import, onchar=ids fonts]{english}
\babelfont{rm}{Noto Sans}
\usepackage{amsmath}
\usepackage{booktabs}
\usepackage{xcolor}
\usepackage{enumitem}
\usepackage{hyperref}

\hypersetup{
    colorlinks=true,
    linkcolor=blue!70!black,
    urlcolor=blue!70!black,
    pdftitle={Bahundanda Electrification Technical Design Basis}
}

\title{\textbf{Bahundanda Electrification Project}\\[0.4em] \large Technical Scope \& Design Basis}
\author{Engineering Design Team}
\date{\today}

\begin{document}

\maketitle

\section{Project Summary \& Scope}
\begin{itemize}[leftmargin=*]
    \item \textbf{Scope:} Supply 68 households (100\,W each, 6.8\,kW total load) on the south spur below Bahundanda bazaar. The maximum allowable voltage-drop limit is 5.0\%. Network routing is derived from a desktop survey.
    \item \textbf{System Design:} A 269\,m, 11\,kV tap line (ACSR Squirrel) from the existing NEA feeder feeds a 25\,kVA, 11/0.4\,kV Dyn11 transformer (T1). Distribution consists of four radial LV feeders (A through D) across 53 poles.
    \item \textbf{Voltage Drop Analysis:} Hand calculations and independent sweep indicate a worst-case voltage drop of 2.3\% from the T1 LV bus and approximately 3.7\% from the 11\,kV source, successfully meeting the 5.0\% limit at 100\,W per household.
    \item \textbf{ETAP Simulations:} Unbalanced load flow (100\% and 150\% load levels), 3-phase and 1-phase short-circuit calculations, and Star protection coordination have been conducted. 3-phase fault calculations align with hand calculations within approximately 3.0\%.
    \item \textbf{Data Discrepancy Notice:} Far-end ETAP results require correction. Load-flow cable drops and 1-phase fault currents indicate swapped branch cable lengths (Section 4.4). Conductor lengths must be updated and studies rerun prior to final report submission.
    \item \textbf{Protection Coordination:} High-voltage K-link fuse (6K class) and a 16\,A MCCB on each outgoing LV feeder coordinate in ETAP Star. Final parameter adjustments remain pending.
    \item \textbf{Growth Margin:} System capacity margin is tight; measured from the 11\,kV source, the 5.0\% voltage-drop threshold is reached at approximately 140\,W per household.
    \item \textbf{Cost Estimate:} Total project cost is Rs~34,05,433 (approximately Rs~50,080 per household, unchanged from Handover 1).
\end{itemize}

\section{Design Basis}

\subsection{Network Configuration}
\begin{itemize}[leftmargin=*]
    \item \textbf{Upstream Source (Assumed):} Tapped from existing NEA 11\,kV feeder at tap pole HT00 ($28.34271^\circ\text{N}$, $84.40667^\circ\text{E}$, elevation $\sim$1,279\,m) equipped with a 3-pole Air Break Switch (ABS).
    \item \textbf{11\,kV Line (HT00 to T1):} 269\,m, 3-phase ACSR Squirrel conductor.
    \item \textbf{Transformer Substation T1:} 25\,kVA, 11/0.4\,kV, Dyn11 vector group, mounted on a double-pole structure with Drop-Out (DO) fuses, 9\,kV surge arresters, and an LV feeder box providing 4 MCCB outgoing ways.
    \item \textbf{LV Distribution Network:} Four radial feeders across 53 LV poles. ACSR Gopher is used from T1 to pole D06; ACSR Squirrel is used on all remaining sections. Phase mapping: Red~=~Feeder~A, Yellow~=~Feeder~B, Blue~=~Feeder~C.
\end{itemize}

\subsection{Impedance Data}
The conductor parameters and equipment impedances utilized in the analytical calculations and ETAP models are structured in Table~\ref{tab:impedance}.

\begin{table}[h!]
\centering
\caption{Electrical Impedance Parameters}
\label{tab:impedance}
\vspace{0.5em}
\begin{tabular}{l c c p{7.2cm}}
\toprule
\textbf{Element} & \textbf{R ($\Omega$/km)} & \textbf{X ($\Omega$/km)} & \textbf{Notes} \\
\midrule
Squirrel, LV & 1.374 & 0.324 & Reactance $X$ from $\text{GMR} = 0.726 r$, 0.4\,m phase spacing \\
Squirrel, 11\,kV & 1.374 & 0.382 & 1.0\,m phase spacing; $Z_0 = 3 \times Z_1$ \\
Gopher, LV & 1.093 & 0.317 & Segment T1 to pole D06 only \\
T1 to A08 ($Z_0$) & 5.496 & 1.296 & $Z_0 = 4 \times Z_1$: Full-size neutral earthed at T1 only \\
T1 to D06 ($Z_0$) & 4.372 & 1.268 & $Z_0 = 4 \times Z_1$: Full-size neutral earthed at T1 only \\
T1 Transformer & -- & -- & 4.0\% impedance, $X/R = 1.0$, $Z_0 = Z_1$, solidly earthed star, tap 0 (typical standard values) \\
Source U1 & -- & -- & 25\,MVA 3-phase and 1-phase short-circuit capacity, $X/R = 2.0$, 1.00\,pu nominal voltage (assumed) \\
\bottomrule
\end{tabular}
\end{table}

\subsection{Main Assumptions}
\begin{itemize}[leftmargin=*]
    \item \textbf{Desktop Survey:} Pole positions and span lengths are derived from remote mapping and are subject to physical ground verification.
    \item \textbf{Consumer Load Profile:} Modeled at 100\,W per household with a power factor ($\cos\phi$) of 0.8 lagging, treated as constant-power loads.
    \item \textbf{Grid Source Parameters:} Point of coupling, fault capacity, and conductor configuration are assumed pending official confirmation from NEA.
    \item \textbf{Transformer Impedance:} Standard typical transformer values are assumed prior to factory test report availability.
\end{itemize}

\end{document}
