# ASFPM Webinar — Building a HEC-RAS 2D Model on the NEER Platform

This repository accompanies the ASFPM webinar demonstration on how to build a
**HEC-RAS 2D hydraulic model** using the [NEER](https://aip.neer.ai/) AI platform.

Follow the step-by-step instructions below to reproduce the demo, from creating
your account to generating flood depth rasters. All you need is the
`project_boundary.geojson` file included in this repository.

---

## What you'll build

Using the NEER platform's AI agent, you'll create a HEC-RAS 2D model of the
Blacksburg, VA study area and produce flood depth rasters for the **100-year
flood event**, with:

- **No culvert burn**
- **No break lines**
- **10-meter DEM** terrain
- **100 ft × 100 ft computational mesh**

---

## What you need

- A modern web browser
- The **`project_boundary.geojson`** link from this repository (you'll paste it
  directly into the agent chatbox — no download required):

  ```
  https://github.com/neeraip/ASFPM_Webinar/blob/main/project_boundary.geojson
  ```
- *(Optional)* A local install of [HEC-RAS](https://www.hec.usace.army.mil/software/hec-ras/)
  if you'd like to run the model on your own machine instead of on the platform

---

## Step-by-step instructions

### 1. Register on the NEER platform

1. Go to **[https://aip.neer.ai/](https://aip.neer.ai/)**.
2. Click **Register / Sign up** and create your account with your email address.

### 2. Verify your account

1. Check your email inbox for a verification message from NEER.
2. Click the verification link to activate your account.
3. Return to [https://aip.neer.ai/](https://aip.neer.ai/) and log in.

### 3. Create a new project

1. Once logged in, make sure you are under your **Personal** account.
2. Click **New Project** (or the **+** button).
3. Give the project a name (for example, `ASFPM Webinar Demo`) and create it.

### 4. Open the project

Click on the project you just created to open its workspace. This is where the
AI agent lives and where your data and models will appear.

### 5. Upload the project boundary

1. Copy the project boundary GeoJSON link from this repository:

   ```
   https://github.com/neeraip/ASFPM_Webinar/blob/main/project_boundary.geojson
   ```
2. In the project workspace, paste the link into the agent chatbox and ask the
   agent to upload it, for example:

   > **Upload this project boundary GeoJSON to the project:
   > https://github.com/neeraip/ASFPM_Webinar/blob/main/project_boundary.geojson**

### 6. Ask the agent to create the HEC-RAS 2D model

With the boundary uploaded, ask the agent to build the model. Use a prompt like:

> **Create a HEC-RAS 2D model for the 100-year flood event, using a 10-meter
> DEM, with no culvert burn, no break lines, and a 100 ft by 100 ft mesh.**

The agent will assemble terrain, boundary conditions, and the 2D flow area, then
build the model to your specifications:

| Setting        | Value                 |
| -------------- | --------------------- |
| Model type     | HEC-RAS 2D            |
| Flood event    | 100-year              |
| Terrain (DEM)  | 10-meter              |
| Culvert burn   | None                  |
| Break lines    | None                  |
| Mesh cell size | 100 ft × 100 ft       |

### 7. Run the model

Once the model is generated, you have two options:

- **Run on the platform** — ask the agent to run the simulation:

  > **Run the model.**

- **Run locally** — download the generated HEC-RAS model from the platform and
  open/run it in your local HEC-RAS install.

### 8. Generate and upload depth rasters

After the simulation finishes, ask the agent to produce the flood depth rasters:

> **Upload the depth rasters.**

The depth rasters visualize inundation extents and water depths across the study
area for the 100-year event.

---

## Files in this repository

| File                       | Description                                            |
| -------------------------- | ------------------------------------------------------ |
| `project_boundary.geojson` | Project boundary polygon for the Blacksburg study area |
| `README.md`                | This guide                                             |

---

## About

Created for the **ASFPM webinar** so attendees can follow along and build their
own HEC-RAS 2D model on the NEER platform. Learn more at
[https://aip.neer.ai/](https://aip.neer.ai/).
