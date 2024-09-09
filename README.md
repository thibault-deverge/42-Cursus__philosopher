# <img src="https://logowik.com/content/uploads/images/423918.logowik.com.webp" style="width: 40px; height: auto;"> This project is part of my curriculum at School 42 <img src="https://logowik.com/content/uploads/images/423918.logowik.com.webp" style="width: 40px; height: auto;">

## About This Project

The Philosophers project is part of the 42 curriculum. The main goal is to simulate the dining philosophers problem, a classic synchronization issue in computer science, using threads and mutexes. The project serves as an introduction to multithreading, thread synchronization, and resource management in C.

In this simulation, multiple philosophers sit around a table, alternating between eating, thinking, and sleeping. The challenge is to avoid deadlocks and starvation while sharing forks (resources) among the philosophers.

[Dining Philosophers Problem](https://en.wikipedia.org/wiki/Dining_philosophers_problem)

## Running the Program

1. `git clone https://github.com/thibault-deverge/42-Cursus__philosopher philosopher`
2. `cd philosopher`
3. `make`

Then the program expects the following arguments:

4. `./philo <number_of_philosophers> <time_to_die> <time_to_eat> <time_to_sleep> [number_of_times_each_philosopher_must_eat]`

- `number_of_philosophers`: The number of philosophers (and forks).
- `time_to_die (in milliseconds)`: Time after a philosopher's last meal before they die if they don't eat.
- `time_to_eat (in milliseconds)`: Time it takes for a philosopher to eat.
- `time_to_sleep (in milliseconds)`: Time a philosopher will spend sleeping.
- `number_of_times_each_philosopher_must_eat` (optional): If provided, the simulation stops when each philosopher has eaten this many times.

### Exemples

`./philo 5 800 200 200 6`

## Output:

The program logs various actions taken by the philosophers:

- When a philosopher takes a fork.
- When a philosopher starts eating.
- When a philosopher starts sleeping.
- When a philosopher starts thinking.
- When a philosopher dies (if applicable).

## Requirements

- The program must handle multiple threads.
- Each philosopher represents a thread, and forks are protected with mutexes to avoid race conditions (tested with hellgrind).
- External functions allowed : `pthread_create`, `pthread_detach`, `pthread_join`, `pthread_mutex_init`, `pthread_mutex_lock`, `pthread_mutex_unlock`, `pthread_mutex_destroy`, `usleep`, `gettimeofday`, `malloc`, `free`, `write`
