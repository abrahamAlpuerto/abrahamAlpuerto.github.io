---
layout: page
title: C++ Chess Engine
description: High-performance chess engine with custom AI opponent
img: assets/img/chess/thumbnail.jpg
importance: 4
category: fun
repositories:
  - https://github.com/abrahamAlpuerto/ChessEngine0
---

This project is a high-performance chess engine and fully functional game board developed in **C++**. It demonstrates low-level systems programming, memory management, and the implementation of classic game theory algorithms.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/chess/board_state.jpg" title="Chess Board Interface" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/chess/terminal_output.jpg" title="Engine Output" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The engine handles move generation, validation, and AI decision-making.
</div>

### Technical Implementation
The core of the engine focuses on efficiency and search depth.
* **Language:** C++
* **Move Generation:** Implements rigorous move validation for all pieces, including special moves like castling, en passant, and promotion.
* **AI Opponent:** Features an AI capable of playing against a human user, utilizing search algorithms to evaluate board states and select optimal moves.

You can view the source code and build instructions on GitHub:
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
    {% include repository/repo.liquid repository="abrahamAlpuerto/ChessEngine0" %}
</div>