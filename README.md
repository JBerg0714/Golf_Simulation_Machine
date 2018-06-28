# Golf Ball Trajectory Simulator
### this is the synopsis of the project - professional 


- create links to other files (hyperlinks) 



- [word/title] (link)



% Default to the notebook output style

    


% Inherit from the specified cell style.




    
\documentclass[11pt]{article}

    
    
    \usepackage[T1]{fontenc}
    % Nicer default font than Computer Modern for most use cases
    \usepackage{palatino}

    % Basic figure setup, for now with no caption control since it's done
    % automatically by Pandoc (which extracts ![](path) syntax from Markdown).
    \usepackage{graphicx}
    % We will generate all images so they have a width \maxwidth. This means
    % that they will get their normal width if they fit onto the page, but
    % are scaled down if they would overflow the margins.
    \makeatletter
    \def\maxwidth{\ifdim\Gin@nat@width>\linewidth\linewidth
    \else\Gin@nat@width\fi}
    \makeatother
    \let\Oldincludegraphics\includegraphics
    % Set max figure width to be 80% of text width, for now hardcoded.
    \renewcommand{\includegraphics}[1]{\Oldincludegraphics[width=.8\maxwidth]{#1}}
    % Ensure that by default, figures have no caption (until we provide a
    % proper Figure object with a Caption API and a way to capture that
    % in the conversion process - todo).
    \usepackage{caption}
    \DeclareCaptionLabelFormat{nolabel}{}
    \captionsetup{labelformat=nolabel}

    \usepackage{adjustbox} % Used to constrain images to a maximum size 
    \usepackage{xcolor} % Allow colors to be defined
    \usepackage{enumerate} % Needed for markdown enumerations to work
    \usepackage{geometry} % Used to adjust the document margins
    \usepackage{amsmath} % Equations
    \usepackage{amssymb} % Equations
    \usepackage{textcomp} % defines textquotesingle
    % Hack from http://tex.stackexchange.com/a/47451/13684:
    \AtBeginDocument{%
        \def\PYZsq{\textquotesingle}% Upright quotes in Pygmentized code
    }
    \usepackage{upquote} % Upright quotes for verbatim code
    \usepackage{eurosym} % defines \euro
    \usepackage[mathletters]{ucs} % Extended unicode (utf-8) support
    \usepackage[utf8x]{inputenc} % Allow utf-8 characters in the tex document
    \usepackage{fancyvrb} % verbatim replacement that allows latex
    \usepackage{grffile} % extends the file name processing of package graphics 
                         % to support a larger range 
    % The hyperref package gives us a pdf with properly built
    % internal navigation ('pdf bookmarks' for the table of contents,
    % internal cross-reference links, web links for URLs, etc.)
    \usepackage{hyperref}
    \usepackage{longtable} % longtable support required by pandoc >1.10
    \usepackage{booktabs}  % table support for pandoc > 1.12.2
    \usepackage[normalem]{ulem} % ulem is needed to support strikethroughs (\sout)
                                % normalem makes italics be italics, not underlines
    

    
    
    % Colors for the hyperref package
    \definecolor{urlcolor}{rgb}{0,.145,.698}
    \definecolor{linkcolor}{rgb}{.71,0.21,0.01}
    \definecolor{citecolor}{rgb}{.12,.54,.11}

    % ANSI colors
    \definecolor{ansi-black}{HTML}{3E424D}
    \definecolor{ansi-black-intense}{HTML}{282C36}
    \definecolor{ansi-red}{HTML}{E75C58}
    \definecolor{ansi-red-intense}{HTML}{B22B31}
    \definecolor{ansi-green}{HTML}{00A250}
    \definecolor{ansi-green-intense}{HTML}{007427}
    \definecolor{ansi-yellow}{HTML}{DDB62B}
    \definecolor{ansi-yellow-intense}{HTML}{B27D12}
    \definecolor{ansi-blue}{HTML}{208FFB}
    \definecolor{ansi-blue-intense}{HTML}{0065CA}
    \definecolor{ansi-magenta}{HTML}{D160C4}
    \definecolor{ansi-magenta-intense}{HTML}{A03196}
    \definecolor{ansi-cyan}{HTML}{60C6C8}
    \definecolor{ansi-cyan-intense}{HTML}{258F8F}
    \definecolor{ansi-white}{HTML}{C5C1B4}
    \definecolor{ansi-white-intense}{HTML}{A1A6B2}

    % commands and environments needed by pandoc snippets
    % extracted from the output of `pandoc -s`
    \providecommand{\tightlist}{%
      \setlength{\itemsep}{0pt}\setlength{\parskip}{0pt}}
    \DefineVerbatimEnvironment{Highlighting}{Verbatim}{commandchars=\\\{\}}
    % Add ',fontsize=\small' for more characters per line
    \newenvironment{Shaded}{}{}
    \newcommand{\KeywordTok}[1]{\textcolor[rgb]{0.00,0.44,0.13}{\textbf{{#1}}}}
    \newcommand{\DataTypeTok}[1]{\textcolor[rgb]{0.56,0.13,0.00}{{#1}}}
    \newcommand{\DecValTok}[1]{\textcolor[rgb]{0.25,0.63,0.44}{{#1}}}
    \newcommand{\BaseNTok}[1]{\textcolor[rgb]{0.25,0.63,0.44}{{#1}}}
    \newcommand{\FloatTok}[1]{\textcolor[rgb]{0.25,0.63,0.44}{{#1}}}
    \newcommand{\CharTok}[1]{\textcolor[rgb]{0.25,0.44,0.63}{{#1}}}
    \newcommand{\StringTok}[1]{\textcolor[rgb]{0.25,0.44,0.63}{{#1}}}
    \newcommand{\CommentTok}[1]{\textcolor[rgb]{0.38,0.63,0.69}{\textit{{#1}}}}
    \newcommand{\OtherTok}[1]{\textcolor[rgb]{0.00,0.44,0.13}{{#1}}}
    \newcommand{\AlertTok}[1]{\textcolor[rgb]{1.00,0.00,0.00}{\textbf{{#1}}}}
    \newcommand{\FunctionTok}[1]{\textcolor[rgb]{0.02,0.16,0.49}{{#1}}}
    \newcommand{\RegionMarkerTok}[1]{{#1}}
    \newcommand{\ErrorTok}[1]{\textcolor[rgb]{1.00,0.00,0.00}{\textbf{{#1}}}}
    \newcommand{\NormalTok}[1]{{#1}}
    
    % Additional commands for more recent versions of Pandoc
    \newcommand{\ConstantTok}[1]{\textcolor[rgb]{0.53,0.00,0.00}{{#1}}}
    \newcommand{\SpecialCharTok}[1]{\textcolor[rgb]{0.25,0.44,0.63}{{#1}}}
    \newcommand{\VerbatimStringTok}[1]{\textcolor[rgb]{0.25,0.44,0.63}{{#1}}}
    \newcommand{\SpecialStringTok}[1]{\textcolor[rgb]{0.73,0.40,0.53}{{#1}}}
    \newcommand{\ImportTok}[1]{{#1}}
    \newcommand{\DocumentationTok}[1]{\textcolor[rgb]{0.73,0.13,0.13}{\textit{{#1}}}}
    \newcommand{\AnnotationTok}[1]{\textcolor[rgb]{0.38,0.63,0.69}{\textbf{\textit{{#1}}}}}
    \newcommand{\CommentVarTok}[1]{\textcolor[rgb]{0.38,0.63,0.69}{\textbf{\textit{{#1}}}}}
    \newcommand{\VariableTok}[1]{\textcolor[rgb]{0.10,0.09,0.49}{{#1}}}
    \newcommand{\ControlFlowTok}[1]{\textcolor[rgb]{0.00,0.44,0.13}{\textbf{{#1}}}}
    \newcommand{\OperatorTok}[1]{\textcolor[rgb]{0.40,0.40,0.40}{{#1}}}
    \newcommand{\BuiltInTok}[1]{{#1}}
    \newcommand{\ExtensionTok}[1]{{#1}}
    \newcommand{\PreprocessorTok}[1]{\textcolor[rgb]{0.74,0.48,0.00}{{#1}}}
    \newcommand{\AttributeTok}[1]{\textcolor[rgb]{0.49,0.56,0.16}{{#1}}}
    \newcommand{\InformationTok}[1]{\textcolor[rgb]{0.38,0.63,0.69}{\textbf{\textit{{#1}}}}}
    \newcommand{\WarningTok}[1]{\textcolor[rgb]{0.38,0.63,0.69}{\textbf{\textit{{#1}}}}}
    
    
    % Define a nice break command that doesn't care if a line doesn't already
    % exist.
    \def\br{\hspace*{\fill} \\* }
    % Math Jax compatability definitions
    \def\gt{>}
    \def\lt{<}
    % Document parameters
    \title{Simulator\_Pres\_JBerg}
    
    
    

    % Pygments definitions
    
\makeatletter
\def\PY@reset{\let\PY@it=\relax \let\PY@bf=\relax%
    \let\PY@ul=\relax \let\PY@tc=\relax%
    \let\PY@bc=\relax \let\PY@ff=\relax}
\def\PY@tok#1{\csname PY@tok@#1\endcsname}
\def\PY@toks#1+{\ifx\relax#1\empty\else%
    \PY@tok{#1}\expandafter\PY@toks\fi}
\def\PY@do#1{\PY@bc{\PY@tc{\PY@ul{%
    \PY@it{\PY@bf{\PY@ff{#1}}}}}}}
\def\PY#1#2{\PY@reset\PY@toks#1+\relax+\PY@do{#2}}

\expandafter\def\csname PY@tok@w\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.73,0.73,0.73}{##1}}}
\expandafter\def\csname PY@tok@c\endcsname{\let\PY@it=\textit\def\PY@tc##1{\textcolor[rgb]{0.25,0.50,0.50}{##1}}}
\expandafter\def\csname PY@tok@cp\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.74,0.48,0.00}{##1}}}
\expandafter\def\csname PY@tok@k\endcsname{\let\PY@bf=\textbf\def\PY@tc##1{\textcolor[rgb]{0.00,0.50,0.00}{##1}}}
\expandafter\def\csname PY@tok@kp\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.00,0.50,0.00}{##1}}}
\expandafter\def\csname PY@tok@kt\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.69,0.00,0.25}{##1}}}
\expandafter\def\csname PY@tok@o\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.40,0.40,0.40}{##1}}}
\expandafter\def\csname PY@tok@ow\endcsname{\let\PY@bf=\textbf\def\PY@tc##1{\textcolor[rgb]{0.67,0.13,1.00}{##1}}}
\expandafter\def\csname PY@tok@nb\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.00,0.50,0.00}{##1}}}
\expandafter\def\csname PY@tok@nf\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.00,0.00,1.00}{##1}}}
\expandafter\def\csname PY@tok@nc\endcsname{\let\PY@bf=\textbf\def\PY@tc##1{\textcolor[rgb]{0.00,0.00,1.00}{##1}}}
\expandafter\def\csname PY@tok@nn\endcsname{\let\PY@bf=\textbf\def\PY@tc##1{\textcolor[rgb]{0.00,0.00,1.00}{##1}}}
\expandafter\def\csname PY@tok@ne\endcsname{\let\PY@bf=\textbf\def\PY@tc##1{\textcolor[rgb]{0.82,0.25,0.23}{##1}}}
\expandafter\def\csname PY@tok@nv\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.10,0.09,0.49}{##1}}}
\expandafter\def\csname PY@tok@no\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.53,0.00,0.00}{##1}}}
\expandafter\def\csname PY@tok@nl\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.63,0.63,0.00}{##1}}}
\expandafter\def\csname PY@tok@ni\endcsname{\let\PY@bf=\textbf\def\PY@tc##1{\textcolor[rgb]{0.60,0.60,0.60}{##1}}}
\expandafter\def\csname PY@tok@na\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.49,0.56,0.16}{##1}}}
\expandafter\def\csname PY@tok@nt\endcsname{\let\PY@bf=\textbf\def\PY@tc##1{\textcolor[rgb]{0.00,0.50,0.00}{##1}}}
\expandafter\def\csname PY@tok@nd\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.67,0.13,1.00}{##1}}}
\expandafter\def\csname PY@tok@s\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.73,0.13,0.13}{##1}}}
\expandafter\def\csname PY@tok@sd\endcsname{\let\PY@it=\textit\def\PY@tc##1{\textcolor[rgb]{0.73,0.13,0.13}{##1}}}
\expandafter\def\csname PY@tok@si\endcsname{\let\PY@bf=\textbf\def\PY@tc##1{\textcolor[rgb]{0.73,0.40,0.53}{##1}}}
\expandafter\def\csname PY@tok@se\endcsname{\let\PY@bf=\textbf\def\PY@tc##1{\textcolor[rgb]{0.73,0.40,0.13}{##1}}}
\expandafter\def\csname PY@tok@sr\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.73,0.40,0.53}{##1}}}
\expandafter\def\csname PY@tok@ss\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.10,0.09,0.49}{##1}}}
\expandafter\def\csname PY@tok@sx\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.00,0.50,0.00}{##1}}}
\expandafter\def\csname PY@tok@m\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.40,0.40,0.40}{##1}}}
\expandafter\def\csname PY@tok@gh\endcsname{\let\PY@bf=\textbf\def\PY@tc##1{\textcolor[rgb]{0.00,0.00,0.50}{##1}}}
\expandafter\def\csname PY@tok@gu\endcsname{\let\PY@bf=\textbf\def\PY@tc##1{\textcolor[rgb]{0.50,0.00,0.50}{##1}}}
\expandafter\def\csname PY@tok@gd\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.63,0.00,0.00}{##1}}}
\expandafter\def\csname PY@tok@gi\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.00,0.63,0.00}{##1}}}
\expandafter\def\csname PY@tok@gr\endcsname{\def\PY@tc##1{\textcolor[rgb]{1.00,0.00,0.00}{##1}}}
\expandafter\def\csname PY@tok@ge\endcsname{\let\PY@it=\textit}
\expandafter\def\csname PY@tok@gs\endcsname{\let\PY@bf=\textbf}
\expandafter\def\csname PY@tok@gp\endcsname{\let\PY@bf=\textbf\def\PY@tc##1{\textcolor[rgb]{0.00,0.00,0.50}{##1}}}
\expandafter\def\csname PY@tok@go\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.53,0.53,0.53}{##1}}}
\expandafter\def\csname PY@tok@gt\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.00,0.27,0.87}{##1}}}
\expandafter\def\csname PY@tok@err\endcsname{\def\PY@bc##1{\setlength{\fboxsep}{0pt}\fcolorbox[rgb]{1.00,0.00,0.00}{1,1,1}{\strut ##1}}}
\expandafter\def\csname PY@tok@kc\endcsname{\let\PY@bf=\textbf\def\PY@tc##1{\textcolor[rgb]{0.00,0.50,0.00}{##1}}}
\expandafter\def\csname PY@tok@kd\endcsname{\let\PY@bf=\textbf\def\PY@tc##1{\textcolor[rgb]{0.00,0.50,0.00}{##1}}}
\expandafter\def\csname PY@tok@kn\endcsname{\let\PY@bf=\textbf\def\PY@tc##1{\textcolor[rgb]{0.00,0.50,0.00}{##1}}}
\expandafter\def\csname PY@tok@kr\endcsname{\let\PY@bf=\textbf\def\PY@tc##1{\textcolor[rgb]{0.00,0.50,0.00}{##1}}}
\expandafter\def\csname PY@tok@bp\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.00,0.50,0.00}{##1}}}
\expandafter\def\csname PY@tok@vc\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.10,0.09,0.49}{##1}}}
\expandafter\def\csname PY@tok@vg\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.10,0.09,0.49}{##1}}}
\expandafter\def\csname PY@tok@vi\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.10,0.09,0.49}{##1}}}
\expandafter\def\csname PY@tok@sb\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.73,0.13,0.13}{##1}}}
\expandafter\def\csname PY@tok@sc\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.73,0.13,0.13}{##1}}}
\expandafter\def\csname PY@tok@s2\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.73,0.13,0.13}{##1}}}
\expandafter\def\csname PY@tok@sh\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.73,0.13,0.13}{##1}}}
\expandafter\def\csname PY@tok@s1\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.73,0.13,0.13}{##1}}}
\expandafter\def\csname PY@tok@mb\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.40,0.40,0.40}{##1}}}
\expandafter\def\csname PY@tok@mf\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.40,0.40,0.40}{##1}}}
\expandafter\def\csname PY@tok@mh\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.40,0.40,0.40}{##1}}}
\expandafter\def\csname PY@tok@mi\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.40,0.40,0.40}{##1}}}
\expandafter\def\csname PY@tok@il\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.40,0.40,0.40}{##1}}}
\expandafter\def\csname PY@tok@mo\endcsname{\def\PY@tc##1{\textcolor[rgb]{0.40,0.40,0.40}{##1}}}
\expandafter\def\csname PY@tok@ch\endcsname{\let\PY@it=\textit\def\PY@tc##1{\textcolor[rgb]{0.25,0.50,0.50}{##1}}}
\expandafter\def\csname PY@tok@cm\endcsname{\let\PY@it=\textit\def\PY@tc##1{\textcolor[rgb]{0.25,0.50,0.50}{##1}}}
\expandafter\def\csname PY@tok@cpf\endcsname{\let\PY@it=\textit\def\PY@tc##1{\textcolor[rgb]{0.25,0.50,0.50}{##1}}}
\expandafter\def\csname PY@tok@c1\endcsname{\let\PY@it=\textit\def\PY@tc##1{\textcolor[rgb]{0.25,0.50,0.50}{##1}}}
\expandafter\def\csname PY@tok@cs\endcsname{\let\PY@it=\textit\def\PY@tc##1{\textcolor[rgb]{0.25,0.50,0.50}{##1}}}

\def\PYZbs{\char`\\}
\def\PYZus{\char`\_}
\def\PYZob{\char`\{}
\def\PYZcb{\char`\}}
\def\PYZca{\char`\^}
\def\PYZam{\char`\&}
\def\PYZlt{\char`\<}
\def\PYZgt{\char`\>}
\def\PYZsh{\char`\#}
\def\PYZpc{\char`\%}
\def\PYZdl{\char`\$}
\def\PYZhy{\char`\-}
\def\PYZsq{\char`\'}
\def\PYZdq{\char`\"}
\def\PYZti{\char`\~}
% for compatibility with earlier versions
\def\PYZat{@}
\def\PYZlb{[}
\def\PYZrb{]}
\makeatother


    % Exact colors from NB
    \definecolor{incolor}{rgb}{0.0, 0.0, 0.5}
    \definecolor{outcolor}{rgb}{0.545, 0.0, 0.0}



    
    % Prevent overflowing lines due to hard-to-break entities
    \sloppy 
    % Setup hyperref package
    \hypersetup{
      breaklinks=true,  % so long urls are correctly broken across lines
      colorlinks=true,
      urlcolor=urlcolor,
      linkcolor=linkcolor,
      citecolor=citecolor,
      }
    % Slightly bigger margins than the latex defaults
    
    \geometry{verbose,tmargin=1in,bmargin=1in,lmargin=1in,rmargin=1in}
    
    

    \begin{document}
    
    
    \maketitle
    
    

    
    \begin{Verbatim}[commandchars=\\\{\}]
{\color{incolor}In [{\color{incolor}1}]:} \PY{c+c1}{\PYZsh{}\PYZsh{} import pandas as pd}
        \PY{k+kn}{import} \PY{n+nn}{numpy} \PY{k}{as} \PY{n+nn}{np}
        \PY{k+kn}{import} \PY{n+nn}{matplotlib}\PY{n+nn}{.}\PY{n+nn}{pyplot} \PY{k}{as} \PY{n+nn}{plt} \PY{c+c1}{\PYZsh{}used for graphing}
\end{Verbatim}

    \begin{Verbatim}[commandchars=\\\{\}]
{\color{incolor}In [{\color{incolor}2}]:} \PY{c+c1}{\PYZsh{}show graphs inline (do not use for print publication quality graphs)}
        \PY{o}{\PYZpc{}}\PY{k}{matplotlib} inline
\end{Verbatim}

    \begin{Verbatim}[commandchars=\\\{\}]
{\color{incolor}In [{\color{incolor}3}]:} \PY{k+kn}{import} \PY{n+nn}{io}
        \PY{k+kn}{import} \PY{n+nn}{base64}
        \PY{k+kn}{from} \PY{n+nn}{IPython}\PY{n+nn}{.}\PY{n+nn}{display} \PY{k}{import} \PY{n}{HTML}
\end{Verbatim}

    \hypertarget{reverse-engineering-a-golf-simulator}{%
\section{Reverse Engineering a Golf
Simulator}\label{reverse-engineering-a-golf-simulator}}

\hypertarget{joshua-berg}{%
\subsection{Joshua Berg}\label{joshua-berg}}

    \hypertarget{goal}{%
\subsection{Goal}\label{goal}}

The initial goal of this research was to reverse engineer an HD golf
simulator to determine the computational model to show the trajectory of
a golf ball while in flight. The idea was to take the output of data
from the simulator itself and use the velocity, apex/peak, carry, launch
angle and spin values to plug into physical equations to compare the
computational trajectory of the golf ball to the trajectory of the
golfball depicted on the screen of the simulator. The idea was to keep
to look at shots with purely backspin to prevent having to analyze the
data within 3-dimensions.

    \hypertarget{using-hd-golf-simulator}{%
\subsection{Using HD Golf Simulator}\label{using-hd-golf-simulator}}

\hypertarget{swinging}{%
\subsubsection{Swinging:}\label{swinging}}

The device used was a High Definition Golf Simulator with video and
forceplate analysis that is located in the Biomechanics Lab on High
Point University's campus. The video below provides a visual example of
how the simulator was used to collect data.

    \begin{Verbatim}[commandchars=\\\{\}]
{\color{incolor}In [{\color{incolor}4}]:} \PY{k+kn}{from} \PY{n+nn}{IPython}\PY{n+nn}{.}\PY{n+nn}{display} \PY{k}{import} \PY{n}{YouTubeVideo}
        \PY{n}{YouTubeVideo}\PY{p}{(}\PY{l+s+s1}{\PYZsq{}}\PY{l+s+s1}{ebIrNY8LZyQ}\PY{l+s+s1}{\PYZsq{}}\PY{p}{)} 
        \PY{c+c1}{\PYZsh{} this was used for presentation in order to avoid having to open another tab outside of the presentation}
\end{Verbatim}
\texttt{\color{outcolor}Out[{\color{outcolor}4}]:}
    
    \begin{center}
    \adjustimage{max size={0.9\linewidth}{0.9\paperheight}}{output_6_0.jpeg}
    \end{center}
    { \hspace*{\fill} \\}
    

    https://www.youtube.com/watch?v=ebIrNY8LZyQ

    The video below shows the trajectory line of the the golf shot taken in
the previous video.

    \begin{Verbatim}[commandchars=\\\{\}]
{\color{incolor}In [{\color{incolor}5}]:} \PY{n}{YouTubeVideo}\PY{p}{(}\PY{l+s+s1}{\PYZsq{}}\PY{l+s+s1}{TZkbjIEdNis}\PY{l+s+s1}{\PYZsq{}}\PY{p}{)}
        \PY{c+c1}{\PYZsh{} this was used for presentation in order to avoid having to open another tab outside of the presentation}
\end{Verbatim}
\texttt{\color{outcolor}Out[{\color{outcolor}5}]:}
    
    \begin{center}
    \adjustimage{max size={0.9\linewidth}{0.9\paperheight}}{output_9_0.jpeg}
    \end{center}
    { \hspace*{\fill} \\}
    

    https://www.youtube.com/watch?v=TZkbjIEdNis

    \hypertarget{initial-data-collection}{%
\subsection{Initial Data Collection}\label{initial-data-collection}}

Following each shot, the simulator would output the following data onto
a computer that was attatched to the simulator. This data was organized
within an excel spreadsheet to more easily identify trends between shots
that were ``elite'' and shots that were ``sub-par''.

    \hypertarget{important-to-note}{%
\subsection{IMPORTANT TO NOTE:}\label{important-to-note}}

\begin{itemize}
\tightlist
\item
  The only shot data that was used for comparison were those with no
  sidespin - only backspin ( 0.0\(^\circ\) - 0.3\(^\circ\))
\item
  An M2 Taylormade Pitching wedge was used for each trial(45\(^\circ\))
\end{itemize}

    \hypertarget{forces-on-the-ball}{%
\subsection{Forces on the ball}\label{forces-on-the-ball}}

\hypertarget{gravity}{%
\subsubsection{Gravity}\label{gravity}}

\[ \vec{F}_{grav} = m \vec{g} \]

\hypertarget{magnus-force-lift}{%
\subsubsection{Magnus Force (Lift)}\label{magnus-force-lift}}

\[ \vec{F}_{lift} = \frac{1}{2}C_m\rho AR\vec{\omega}\times \vec{v} \]

where:

\begin{itemize}
\tightlist
\item
  \(\rho\) - Density of air
\item
  \(C_m\) - Lift Coefficient
\item
  \(A\) - Cross Sectional Area
\item
  \(\vec{v}\) - Velocity of ball
\item
  \(\vec{\omega}\) - Spin velocity
\end{itemize}

\hypertarget{drag-force}{%
\subsubsection{Drag Force}\label{drag-force}}

\[\vec{F}_d = \frac{1}{2}C_d\rho Av\vec{v}\]

source referenced:
https://github.com/JBerg0714/Golf\_Simulation\_Machine/blob/master/Source\%20that\%20was\%20referenced.pdf

    \hypertarget{initial-trials}{%
\subsection{INITIAL TRIALS}\label{initial-trials}}

    \hypertarget{first-set-of-trials}{%
\subsection{First Set of Trials}\label{first-set-of-trials}}

The red dots are individuals points taken from the trajectory of the
golf ball provided by the simulator. The blue line is the expected
trajectory of the golf ball using the values output by the simulator
that were plugged into the force equations that were shown above. Some
of these values were: \#\#\#\# - velocity (vector) \#\#\#\# - spin rate

Link to the jupyter notebook used:
https://github.com/JBerg0714/Golf\_Simulation\_Machine/blob/master/Jupyter\%20Notebooks\%20/golf-ball-rk4-v3.ipynb

    \hypertarget{calculating-rms}{%
\subsection{Calculating RMS}\label{calculating-rms}}

RMS Definition: The square \textbf{root} of the \textbf{mean} of the sum
of the \textbf{square} of the distance between the model points and the
HD Golf points for both the peak and the end.

\hypertarget{peak-of-the-shot}{%
\subsubsection{Peak of the shot}\label{peak-of-the-shot}}

\[ dP^2 = (X_{peak_{HD}} - X_{apex_{model}})^2 + (Y_{apex_{HD}} - Y_{apex_{model}})^2\]

\hypertarget{end-point-of-the-shot}{%
\subsubsection{End Point of the shot}\label{end-point-of-the-shot}}

\[ dE^2 = (x_{end_{HD}} - x_{end_{model}})^2 + (y_{end_{model}})^2 \]

\hypertarget{rms-of-the-shot}{%
\subsubsection{RMS of the shot}\label{rms-of-the-shot}}

\[ RMS = \sqrt{\frac{dP^2 + dE^2}{2}} \]

    The image above shows a trial where there were clear differences in the
simulator trajectory line and computational model trajectory line. The
difference between the two trend lines is represented by the RMS values
discussed in the previous slide.

    \hypertarget{rms-for-one-trial}{%
\subsubsection{RMS for one trial:}\label{rms-for-one-trial}}

\hypertarget{using-manually-altered-parameters}{%
\paragraph{Using Manually altered
parameters}\label{using-manually-altered-parameters}}

There coefficient for lift and drag was unknown. In order to solve for
the combinations of coefficients that led to the lowest average RMS
value for the first 12 trials, the coefficients were manually changed
and applied to all trials. The following were the initial coefficients
provided the lowest average RMS value:

\begin{itemize}
\tightlist
\item
  \(C_d\) - 0.36
\item
  \(C_m\) - 0.50
\end{itemize}

For each trial the RMS values were calculated and were printed out like
the following:

\hypertarget{average-rms-for-the-first-12-trials-3.371-m}{%
\subsubsection{Average RMS for the first 12 trials: 3.371
m}\label{average-rms-for-the-first-12-trials-3.371-m}}

This means that the average difference in the trend line for the
simulator and computational model was 3.37 meters.

Link to the jupyter notebook used:
https://github.com/JBerg0714/Golf\_Simulation\_Machine/blob/master/Jupyter\%20Notebooks\%20/golf-ball-rk4-v4.ipynb

    \hypertarget{optimization-of-coefficients}{%
\subsection{Optimization of
coefficients}\label{optimization-of-coefficients}}

A sub-goal for this project was to make the computational model
autonomous. In other words, to find the best pair of coefficients that
led to the lowest RMS values.

\hypertarget{using-scipy}{%
\subsubsection{Using Scipy}\label{using-scipy}}

The Scipy function was used to find these values.

\hypertarget{best-coefficients}{%
\paragraph{Best coefficients:}\label{best-coefficients}}

\begin{itemize}
\tightlist
\item
  \(C_d\) - 0.41123417\\
\item
  \(C_m\) - 0.59101698
\end{itemize}

Link to jupyter notebook used:
https://github.com/JBerg0714/Golf\_Simulation\_Machine/blob/master/Jupyter\%20Notebooks\%20/golf-ball-rk4-v5.ipynb

    \hypertarget{applied-trials}{%
\subsection{APPLIED TRIALS}\label{applied-trials}}

    \hypertarget{using-optimized-parameters}{%
\subsection{Using Optimized
Parameters}\label{using-optimized-parameters}}

After autonomously finding the best coefficents for drag and lift,
another set of trials were taken and these values were applied to get
another RMS average.

\hypertarget{average-rms-for-second-set-of-12-trials-3.861-m}{%
\paragraph{Average RMS for second set of 12 trials: 3.861
m}\label{average-rms-for-second-set-of-12-trials-3.861-m}}

It was found that for shots with spin rates larger than 9000 rpm, the
RMS values were larger.

Link to jupyter notebook used:
https://github.com/JBerg0714/Golf\_Simulation\_Machine/blob/master/Jupyter\%20Notebooks\%20/golf-ball-rk4-v6-(TESTDATA).ipynb

    \hypertarget{conclusion}{%
\subsection{Conclusion}\label{conclusion}}

\hypertarget{percent-difference-of-carry-for-second-set-of-trials}{%
\subsubsection{Percent Difference of Carry for second set of
trials}\label{percent-difference-of-carry-for-second-set-of-trials}}

\[\% Difference = \frac{(x_{end_{HD}} - x_{end_{model}})}{x_{end_{HD}}}\times100 \]

\hypertarget{average-percent-difference-2.705}{%
\paragraph{Average Percent Difference: 2.705
\%}\label{average-percent-difference-2.705}}

This percent difference accounts for the differences in carry between
the simulator and computational carry. Let's say the average golfer can
hit the ball 100 yards with there pitching wedge. This means that with a
2.705 percent difference, the computational model is accurate to within
3 yards of each shot.

\(\textbf{Example:}\)

\(\textit{John's shot with a pitching wedge measured 100 yards by the HD Golf Simulator. This means the computational model we will show the shot being between 97 to 103 yards.}\)

Link to jupyter notebook used:
https://github.com/JBerg0714/Golf\_Simulation\_Machine/blob/master/Jupyter\%20Notebooks\%20/golf-ball-rk4-v10.ipynb

    \hypertarget{in-the-future}{%
\subsection{In the future}\label{in-the-future}}

\begin{itemize}
\item
  Work with a 3 Dimensional Computational Model (Side Spin)
\item
  Account for weather and physical elements such as:
\item
  Wind
\item
  Slopes of course
\item
  Different Lies (Rough, Sand, Fairway)
\item
  Bounce and Roll
\end{itemize}

    \hypertarget{acknowledgments}{%
\section{Acknowledgments}\label{acknowledgments}}

\begin{itemize}
\tightlist
\item
  Vadym from HD Golf
\end{itemize}

Department of Physics, High Point University - Dr.~Aaron Titus

Department of Physical Therapy, High Point University - Dr.~Eric Hegedus


    % Add a bibliography block to the postdoc
    
    
    
    \end{document}
