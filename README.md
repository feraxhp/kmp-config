# KMP config

This action loads all the necessary tools and dependencies for your github 
actions environment to build your __kotlin multiplatform__ project.

## usage
~~~yml
on:
  workflow_dispatch:

jobs:
  sample:
    runs-on: ubuntu-latest
    steps:
      - name: 🗃️ Checkout code
        uses: actions/checkout@v4
      
      - name: ⚙️ KMP Config
        uses: feraxhp/kmp-config@v1.0.0
        with:
          path: ${{ inputs.path }} # Optional path to the project root (defaults to the github.workspace)
~~~

## What is does?

- 🧪 Setup Gradle
    - > uses (gradle/gradle-build-action@v3)
- 📲 Setup Java (version 17)
- 🔓 gradlew (add execute permissions)

## Simple block copy

~~~yml
- name: ⚙️ KMP Config
  uses: feraxhp/kmp-config@v1.0.0
~~~
