# 図の挿入

- [1. プリアンブル](#1-プリアンブル)
- [2. 通常](#2-通常)
- [3. トリミング](#3-トリミング)
- [4. まとめて横並び](#4-まとめて横並び)

## 1. プリアンブル
```Tex
\usepackage[dvipdfmx]{graphicx}

% キャプションで改行しても中央ぞろえにする
\usepackage{caption}
\captionsetup[figure]{justification=centering}

% まとめて横ならびさせた時のsubcaptionを使う
\usepackage[subrefformat=parens]{subcaption}
```

## 2. 通常
```Tex
\begin{figure}
    \centering
    \includegraphics[width=10cm]{img/img1.png}
    \caption{画像1\linebreak 2行目}
    \label{fig1}
\end{figure}
```

## 3. トリミング
元の画像に対してトリミングを行う．
切り取り幅は左下右上の順で指定する．
```Tex
\begin{figure}
    \centering
    \includegraphics[trim=10 10 10 10, width=10cm]{img/img1.png}
    \caption{画像1\linebreak 2行目}
    \label{fig1}
\end{figure}
```
## 4. まとめて横並び
```Tex
\begin{figure}[h]
    \begin{tabular}{cc}
        \begin{minipage}[b]{0.47\hsize}
            \centering
            \includegraphics[width=6.8cm]{img/1.png}
            \subcaption{画像1}
            \label{fig1a}
        \end{minipage} &
        \begin{minipage}[b]{0.47\hsize}
            \centering
            \includegraphics[width=6.8cm]{img/2.png}
            \subcaption{画像2}
            \label{fig1b}
        \end{minipage}   \\
        \multicolumn{2}{c}{
            \begin{minipage}[b]{0.47\hsize}
                \centering
                \includegraphics[width=6.8cm]{img/3.png}
                \subcaption{画像3}
                \label{fiig1c}
            \end{minipage}
        }
    \end{tabular}
    \caption{画像1-3}
    \label{fig1}
\end{figure}
```