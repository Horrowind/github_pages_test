{% include mathjax.html %}

\(\newcommand\A{\mathcal{A}}
\newcommand\conv{\mathop{conv}} \newcommand\R{\mathbb{R}}
\renewcommand\int{\mathop{int}}
\newcommand\lk{\mathrm{lk}}
\newcommand\rEuler{\tilde{\chi}}\)

Im Seminar *Punktkonfigurationen, Euler-Charakteristiken und Bewertungen* widmen wir uns einem bestimmten Zusammenspiel von geometrischer und topologischer Kombinatorik. Sei \(\A \subset \R^d\) eine endliche Punktkonfiguration. Wir schreiben \(\conv(\A)\) für die konvexe Hülle und \(\int(X)\) für das Innere einer Menge \(X\). Wir nehmen an, dass \(\conv(\A)\) voll-dimensional ist.
Eine Menge \(K \subseteq \A\) heißt **free**, falls \(\conv(K) \cap \A = K\) und \(\conv(K \setminus p) \neq \conv(K)\) für alle \(p \in K\) gilt. Unsere Motivation kommt aus folgender Formel, die in [1] bewiesen wurde:
\[ |\int  \conv(\A) | \ = \ (-1)^{d-1} \sum_{K \text{ free}} (-1)^{|K|} |K| \]

Die erste Perspektive, aus der wir diese Formel betrachten wollen ist kommt aus der topologischen Kombinatorik. Dafür schreiben wir die rechte Seite der Formel um:
\[
\sum_{K \text{ free}} (-1)^{|K|} |K| \ = \
\sum_{K \text{ free}} \sum_{a \in K} (-1)^{|K|}  \ = \
\sum_{a \in \A} \sum_{K \text{ free}, a \in K}  (-1)^{|K|}
\]
Sei \(\Delta = \{ K \subseteq \A : K \text{ free} \}\). Es ist unschwer zu erkennen, dass \( \Delta \) ein Simplizialkomplex ist, also \(\emptyset \in \Delta\) und für alle \(\sigma \in \Delta\) und \(\tau \subseteq \sigma\) gilt \(\tau \in \Delta\). Für ein \(\tau \in \Delta \) definieren wir den **Link** als
\[
\lk_\Delta(\tau) \ := \ \{ \sigma \in \Delta : \sigma \cup \tau \in \Delta, \sigma \cap \tau = \emptyset \}
\]
Die **reduzierte Euler-Charakteristik** eines Simplizialkomplexes \(\Gamma\) ist \(\rEuler(\Gamma) = \sum_{\tau \in \Gamma} (-1)^{|\tau|-1}\). Damit bekommen wir
\[
\sum_{a \in \A} \sum_{K \text{ free}, a \in K}  (-1)^{|K|}
\ = \ \sum_{a \in \A} \rEuler(\lk_\Delta(a))
\]

Für den Beweis der Formel reicht es also zu zeigen, dass \(\rEuler(\lk_\Delta(a)) = (-1)^{d-1}\) falls \(a \in \int\conv(\A)) \) und \(=0\) sonst. Genauer werden wir uns mit der Topologie von \(\Delta\) und \(\lk_\Delta(a)\) beschäftigen, wie es in dem Artikel

[1] Edelman, Reiner "Counting the Interior Points of a Point Configuration"

getan wird.

Der vorläufige Plan dafür ist:
4. Mai (Raman): Wiederholung Simplizialkomplexe und Homologie, Posets und Ordnungskomplexe nach Section 2
11. Mai (Elias+Aenne): Beweis der Formel nach Section 3
18. Mai (Niklas+Sebastian): Erweiterungen auf convex geometries (Sections 4+5)
