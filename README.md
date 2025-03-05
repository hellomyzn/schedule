# docker-html-handson
Markwhenのコンテナ https://markwhen.com/

# Markwhen Syntax Guide

## Overview
Markwhen is a text-based timeline tool that allows you to define events and schedules in a structured way. This guide provides an overview of the basic syntax and features.

## Basic Syntax

### Setting a Title
```
title: Project Development
```

### Defining Events
```
// Date range: Event description #tag
2024-01-01/2024-01-14: Requirements Analysis #requirements_definition
2024-01-15/2024-02-04: Design Phase #design
2024-02-05/2024-02-25: Implementation #implement
2024-02-26/2024-03-17: Testing #test
2024-03-18/2024-03-31: Deployment #deployment
2024-04-01: Release #release
```

### Using Relative Dates and Event IDs
```
2024-12-12/5 days: Event 1 #foo !event1
after !event1/2 days: Event 2 #bar
after !event1/7 days: Event 3 #baz
```

### Recurring Events
```
every 1 week: Weekly recurring event #foo
2025-06-01/3 days every 1 month x10: Monthly recurring event for 3 days, repeated 10 times #bar
```

### Task Lists
```
2024-12-02/3 days: Event 1 #foo
- [x] Task 1
- [x] Task 2
- [ ] Task 3
```

### Using Tags
```
2 days: Event 1 #foo
2 days: Event 2 #bar
2 days: Event 3 #baz
2 days: Event 4 #qux
2 days: Event 5
2 days: Event 6
2 days: Event 7
2 days: Event 8
```

### Sections and Groups
```
section Section 1
  group Group 1
    2 days: Event 1 #foo
    2 days: Event 2 #bar
  endGroup
  group Group 2
    2 days: Event 3 #baz
    2 days: Event 4 #qux
  endGroup
endSection

section Section 2
  group Group 3
    2 days: Event 5
    2 days: Event 6
    group Group 4
      2 days: Event 7
      2 days: Event 8
    endGroup
  endGroup
endSection
```

## Conclusion
Markwhen provides an easy and flexible way to define structured timelines and events. Using this guide, you can create detailed schedules, plan projects, and visualize workflows efficiently.


### Docker Command
```
# build (docker-compose up -d --build)
$ make up

# down (docker-compose down)
$ make down
```

### Into to container
```
# python3 server (docker-compose exec python3 bash)
$ make python
```


### Ruine the world
```
# destroy (docker-compose down --rmi all --volumes --remove-orphans)
$ make destroy
```

### hoge
How do I press and hold a key and have it repeat in VSCode?
```
$ defaults write com.microsoft.VSCode ApplePressAndHoldEnabled -bool false

```
