# http-github.com-JR-M29-repo-Issue-2

*Issue 2:* Notes are not displayed correctly on the page
    - Label: functional
    - Description: When a user saves a note, it is not displayed correctly on the page.


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
