@link
=====

.. important::

   The effects of the inline version of this tag are not yet fully implemented
   in phpDocumentor 3. There's only URI support (i.e. no support for
   Structural Elements), and even that is available only in long descriptions.

The @link tag indicates a custom relation between associated
Structural Elements and a website, which is identified by an absolute
URI.

Syntax
------

    @link [URI] [<description>]

or inline

   {@link [URI] [<description>]}

Description
-----------

The @link tag can be used to define a relation, or link, between
Structural Elements or part of the long description, when used inline,
to an URI.

The URI MUST be complete and well-formed as specified in
`RFC2396 <https://www.ietf.org/rfc/rfc2396.txt>`_.

The @link tag MAY have a description appended to indicate the type of relation
defined by this occurrence.

Effects in phpDocumentor
------------------------

Structural Elements, or inline text in a long description, tagged with
the @link tag will show a link in their description. If a description is
provided with the tag then this will be used as link text instead of the URL itself.

Examples
--------

Normal tag:

.. code-block:: php
   :linenos:

    /**
     * @link https://example.com/my/bar Documentation of Foo.
     *
     * @return integer Indicates the number of items.
     */
    function count()
    {
        <...>
    }

Inline tag:

.. code-block:: php
   :linenos:

    /**
     * This method counts the occurrences of Foo.
     *
     * When no more Foo ({@link https://example.com/my/bar}) are given this
     * function will add one as there must always be one Foo.
     *
     * @return integer Indicates the number of items.
     */
    function count()
    {
        <...>
    }

