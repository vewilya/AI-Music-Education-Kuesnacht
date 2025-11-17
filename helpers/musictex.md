# MusiXTeX First Steps

Quick reference guide for basic music notation in MusiXTeX.

## Package Setup

```latex
\usepackage{musixtex}
```

## Basic Structure

```latex
\begin{music}
\instrumentnumber{1}           % Number of instruments
\setclef1{\treble}            % Set clef (treble, bass, alto, tenor)
\generalmeter{\meterfrac{4}{4}} % Time signature
\startextract
% Your notes here
\endextract
\end{music}
```

## Note Durations

```latex
\wh{c}    % Whole note
\hu{c}    % Half note
\qu{c}    % Quarter note
\cu{c}    % Eighth note
\ccu{c}   % Sixteenth note
```

## Accidentals

```latex
\qu{c}    % C natural
\qu{^c}   % C-sharp (♯)
\qu{_c}   % C-flat (♭)
\qu{=c}   % C-natural (♮) explicit
```

## Octaves

```latex
\qu{c}    % Middle C
\qu{c'}   % One octave higher
\qu{c''}  % Two octaves higher
\qu{c`}   % One octave lower
\qu{c``}  % Two octaves lower
```

## Combining Accidentals and Octaves

```latex
\qu{^f'}   % F-sharp, one octave up
\qu{_b`}   % B-flat, one octave down
\qu{_e''}  % E-flat, two octaves up
```

## Chords

Use `z` prefix for simultaneous notes (chord):

```latex
\zqu{ceg}\qu{c}    % C major chord (C-E-G-C)
\zqu{d_fa}\qu{d}   % D minor chord (D-F-A-D)
\zqu{c^eg'}\qu{c}  % C major with high G
```

## Bar Lines

```latex
\bar      % Single bar line
\endbar   % Final double bar
```

## Complete Example

```latex
\begin{music}
\instrumentnumber{1}
\setclef1{\treble}
\generalmeter{\meterfrac{4}{4}}
\startextract
\Notes\qu{c}\qu{d}\qu{e}\qu{f}\en
\bar
\Notes\qu{g}\qu{a}\qu{b}\qu{c'}\en
\bar
\Notes\wh{c}\wh{c}\en
\endextract
\end{music}
```

## Two Staves (Piano)

```latex
\begin{music}
\instrumentnumber{1}
\setstaffs{1}{2}              % Two staves for instrument 1
\setclef1{\treble}
\setclef2{\bass}
\generalmeter{\meterfrac{4}{4}}
\startextract
\Notes\zqu{ceg}\qu{c}|\zql{C}\qu{E}\en  % | separates staves
\bar
\Notes\wh{c}|\wh{C}\en
\endextract
\end{music}
```

## Common Pitches

**Treble Clef:**
- `c d e f g a b c'` = C4-C5 (middle C to high C)

**Bass Clef:**
- `C D E F G A B c` = C2-C3 (low C to middle C)

## Tips

- End note groups with `\en`
- Use `\Notes...\en` for note groups
- Lower case = higher octave, Upper case = lower octave
- The `|` character separates different staves