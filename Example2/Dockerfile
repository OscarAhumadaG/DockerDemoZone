FROM jupyter/tensorflow-notebook

# Switch to root user
USER root

# Install required packages
RUN pip install --upgrade pip && \
    pip install transformers && \
    pip install pysrt

# Copy the files with root permissions
COPY captions_english.srt Translator.ipynb /home/$NB_USER/

# Set correct ownership and permissions
RUN chown $NB_UID:$NB_GID /home/$NB_USER/captions_english.srt /home/$NB_USER/Translator.ipynb && \
    chmod 644 /home/$NB_USER/captions_english.srt /home/$NB_USER/Translator.ipynb && \
    fix-permissions "/home/${NB_USER}"

# Switch back to the default user
USER $NB_UID

