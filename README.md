I have uploaded the screenshots that you gave me but separately, they are not in any folder. can you write me a code like this so that I can just make the changes easily
# PathWise - AI-Driven Career Guidance and Navigation System

## Introduction

PathWise is a career-guidance web application designed to help engineering students explore roles that may fit their technical skills and interests. The project combines a questionnaire-based career prediction workflow with supporting pages for career information, courses, and learning resources.

The repository uses a PHP website for the main user-facing experience and a Python machine-learning component for career-role prediction.

## Overview

The prediction dataset contains 17 skill-related attributes and a role label. In `testmodel.py`, the data is split into training and test sets, and a K-Nearest Neighbours classifier with five neighbours is trained. The fitted model is saved as `careerlast.pkl`.

The Flask application in `testapp.py` accepts form values, loads the saved model, and returns a predicted role along with other role suggestions derived from the model's probability output. The PHP site provides the main landing page, account registration and login flows, and links to the prediction service and career-resource sections.

A separate experiment in `bagging.py` evaluates a bagging classifier built from decision trees using cross-validation. It is included as an additional modelling experiment rather than being presented as the deployed prediction model.

## Main Functionality

- Register and log in through the PHP website.
- Submit skill-related responses to the career prediction interface.
- Predict a career category from the submitted skill profile.
- Display additional possible roles based on model probability scores.
- Browse career information pages for different professional roles.
- Access course and knowledge-resource sections.

## Implementation

- **Frontend and website:** PHP, HTML, CSS, JavaScript
- **Backend prediction service:** Python, Flask
- **Machine learning:** scikit-learn, K-Nearest Neighbours
- **Data handling:** Pandas, NumPy
- **Model persistence:** Pickle
- **Database:** MySQL

## Running the Project

The repository contains two connected parts: the PHP website and the Flask prediction service. The PHP application requires a local PHP/MySQL environment. The prediction service requires Python dependencies and the model/data files used by the scripts.

The current PHP pages refer to the Flask service at `127.0.0.1:5000`, so both services need to be configured and running locally for the complete flow to work. Update local database settings in `config.php` before starting the website.

## Notes

Career suggestions are model outputs based on the dataset and features used in this project. They are intended as guidance for exploration, not as definitive decisions about a person's career.
