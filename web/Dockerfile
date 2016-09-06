FROM python:2.7

# Set env variables used in this Dockerfile (add a unique prefix, such as DOCKYARD)
# Local directory with project source
ENV DOCKYARD_SRC=webapp

# Directory in container for all project files
ENV DOCKYARD_SRVHOME=/srv

# Directory in container for project source files
ENV DOCKYARD_SRVPROJ=/srv/web

# Copy application source code to SRCDIR
COPY $DOCKYARD_SRC $DOCKYARD_SRVPROJ

# Install Python dependencies
RUN pip install -r $DOCKYARD_SRVPROJ/requirements.txt

# Copy entrypoint script into the image
WORKDIR $DOCKYARD_SRVPROJ
COPY ./entrypoint.sh /
ENTRYPOINT ["/entrypoint.sh"]docker