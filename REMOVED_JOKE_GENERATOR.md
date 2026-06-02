## Removed Files

The following joke generator related files have been removed from the project:

### API Service
- `src/features/jokes/api/jokeService.ts` - Removed
- `src/features/jokes/store/jokeStore.ts` - Removed
- `src/features/jokes/hooks/useJoke.ts` - Removed

### Components
- `src/features/jokes/components/JokeCard.tsx` - Removed
- `src/features/jokes/components/SavedJokeList.tsx` - Removed

### Screens
- `src/app/joke-generator.tsx` - Removed
- `src/app/saved-jokes.tsx` - Removed

### Database
- `scripts/saved-jokes-schema.sql` - Removed

### Documentation
- `docs/JOKE_GENERATOR.md` - Removed

To complete the removal, you may also want to:

1. Delete the `src/features/jokes/` directory entirely
2. Delete the `docs/JOKE_GENERATOR.md` file
3. Remove any navigation routes pointing to joke screens

Note: These files are no longer part of the BK Mine project. The project focuses purely on reservation and queue management for food sellers.
