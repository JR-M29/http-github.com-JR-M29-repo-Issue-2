# http-github.com-JR-M29-repo-Issue-2


describe('Saving and displaying notes', () => {
  it('should display a saved note on the page', () => {
    const note = { title: 'Test Note', content: 'This is a test note' };
    saveNote(note);
    const noteElement = document.querySelector('.note');
    expect(noteElement).toBeInTheDocument();
    expect(noteElement).toHaveTextContent(note.title);
    expect(noteElement).toHaveTextContent(note.content);
  });
});
