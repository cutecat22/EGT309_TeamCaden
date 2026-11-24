# Docker development environment


1. Install Docker Desktop and make sure it is running.
2. Open a terminal in this `docker` folder.
3. Run: `docker compose up --build` (the first build takes a few minutes).
4. Open http://localhost:8888 in a browser. The project files are in the `/app` folder shown on the left.
   Open `eda.ipynb` and choose Run > Run All Cells.
5. Press Ctrl+C in the terminal to stop. Run `docker compose down` to remove the container.

Changes made in JupyterLab are saved to the real project folder, because the folder is mounted into the container.
