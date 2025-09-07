{
 "cells": [
  {
   "cell_type": "markdown",
   "id": "a08d4c25-4842-41c3-8a00-f360f1b35791",
   "metadata": {},
   "source": [
    "# Functional Requirements – Enhanced N-Queens Backend\n",
    "\n",
    "## FR-1: Board Creation\n",
    "- The system shall allow users to create a board.\n",
    "- Two modes supported:\n",
    "  1. **Predefined Board** → user selects `N`, board auto-colored.\n",
    "  2. **Custom Board** → user defines regions/colors manually.\n",
    "\n",
    "## FR-2: Board Representation\n",
    "- Each board shall be stored with:\n",
    "  - Board size `N`\n",
    "  - Region/Color mapping\n",
    "  - Unique **Board ID** for reference\n",
    "\n",
    "## FR-3: Input Constraints\n",
    "- Exactly one queen per row, column, and diagonal.\n",
    "- Exactly one queen per colored region.\n",
    "- For custom boards, user must define valid partitions.\n",
    "\n",
    "## FR-4: Enhanced N-Queens Solver\n",
    "- The solver shall compute **all valid queen placements**.\n",
    "- Solutions must satisfy both standard N-Queens + region constraints.\n",
    "- Algorithm must use **DFS + backtracking**.\n",
    "\n",
    "## FR-5: Solution Storage\n",
    "- Valid solutions shall be associated with the board’s **Board ID**.\n",
    "- Storage may use database or in-memory persistence.\n",
    "\n",
    "## FR-6: Solution Retrieval\n",
    "- The system shall allow fetching all solutions by **Board ID**.\n",
    "- Solutions returned as coordinate arrays or board matrix.\n",
    "\n",
    "## FR-7: Solution Sharing\n",
    "- Each board shall be shareable via **Board ID**.\n",
    "- Friends can fetch and solve using the same ID.\n",
    "\n",
    "## FR-8: API Integration\n",
    "- Backend shall expose APIs for:\n",
    "  - Board creation\n",
    "  - Running solver\n",
    "  - Fetching solutions\n",
    "\n",
    "## FR-9: Error Handling\n",
    "- Invalid board configurations → return descriptive error.\n",
    "- Empty or unsolvable boards → return empty solution set.\n",
    "\n",
    "## FR-10: Performance & Scalability\n",
    "- Solver must handle at least **N=15** within reasonable time.\n",
    "- Support concurrent API requests without conflict.\n",
    "\n",
    "---\n"
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3 (ipykernel)",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.10.9"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
