<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "9b03446058b4eed46928ae5e46325ea0",
  "translation_date": "2025-10-02T11:02:05+00:00",
  "source_file": "00-course-setup/README.md",
  "language_code": "tl"
}
-->
# Pagsisimula ng Kurso

## Panimula

Tatalakayin sa araling ito kung paano patakbuhin ang mga halimbawa ng code para sa kursong ito.

## Sumali sa Iba Pang Mga Mag-aaral at Humingi ng Tulong

Bago mo simulan ang pag-clone ng iyong repository, sumali sa [AI Agents For Beginners Discord channel](https://aka.ms/ai-agents/discord) upang makakuha ng tulong sa setup, magtanong tungkol sa kurso, o makipag-ugnayan sa iba pang mga mag-aaral.

## I-clone o I-fork ang Repository na Ito

Upang magsimula, mangyaring i-clone o i-fork ang GitHub Repository. Sa ganitong paraan, magkakaroon ka ng sariling bersyon ng materyal ng kurso upang maipatupad, masubukan, at mabago ang code!

Magagawa ito sa pamamagitan ng pag-click sa link na ito upang <a href="https://github.com/microsoft/ai-agents-for-beginners/fork" target="_blank">i-fork ang repository</a>.

Dapat ay mayroon ka na ngayong sariling forked na bersyon ng kursong ito sa sumusunod na link:

![Forked Repo](../../../translated_images/forked-repo.33f27ca1901baa6a5e13ec3eb1f0ddd3a44d936d91cc8cfb19bfdb9688bd2c3d.tl.png)

## Pagpapatakbo ng Code

Nag-aalok ang kursong ito ng serye ng mga Jupyter Notebooks na maaari mong gamitin upang magkaroon ng praktikal na karanasan sa paggawa ng AI Agents.

Ang mga halimbawa ng code ay gumagamit ng alinman sa:

**Kailangan ng GitHub Account - Libre**:

1) Semantic Kernel Agent Framework + GitHub Models Marketplace. Tinukoy bilang (semantic-kernel.ipynb)  
2) AutoGen Framework + GitHub Models Marketplace. Tinukoy bilang (autogen.ipynb)

**Kailangan ng Azure Subscription**:  
3) Azure AI Foundry + Azure AI Agent Service. Tinukoy bilang (azureaiagent.ipynb)

Hinihikayat ka naming subukan ang lahat ng tatlong uri ng mga halimbawa upang makita kung alin ang pinakaangkop para sa iyo.

Anuman ang iyong piliin, ito ang magtatakda kung aling mga hakbang sa setup ang kailangan mong sundin sa ibaba:

## Mga Kinakailangan

- Python 3.12+
  - **NOTE**: Kung wala kang naka-install na Python3.12, tiyaking i-install ito. Pagkatapos, gumawa ng iyong venv gamit ang python3.12 upang masiguro na ang tamang mga bersyon ay mai-install mula sa requirements.txt file.
  
    >Halimbawa

    Gumawa ng Python venv directory:

    ``` bash
    python3 -m venv venv
    ```

    Pagkatapos, i-activate ang venv environment para sa:

    macOS at Linux

    ```bash
    source venv/bin/activate
    ```
  
    Windows

    ```bash
    venv\Scripts\activate
    ```

- Isang GitHub Account - Para sa Access sa GitHub Models Marketplace
- Azure Subscription - Para sa Access sa Azure AI Foundry
- Azure AI Foundry Account - Para sa Access sa Azure AI Agent Service

Kasama sa repository na ito ang isang `requirements.txt` file na naglalaman ng lahat ng kinakailangang Python packages upang patakbuhin ang mga halimbawa ng code.

Maaari mong i-install ang mga ito sa pamamagitan ng pagtakbo ng sumusunod na command sa iyong terminal sa root ng repository:

```bash
pip install -r requirements.txt
```
Inirerekomenda naming gumawa ng Python virtual environment upang maiwasan ang anumang mga salungatan at isyu.

## I-setup ang VSCode
Siguraduhing ginagamit mo ang tamang bersyon ng Python sa VSCode.

![image](https://github.com/user-attachments/assets/a85e776c-2edb-4331-ae5b-6bfdfb98ee0e)

## Setup para sa Mga Halimbawa gamit ang GitHub Models 

### Hakbang 1: Kunin ang Iyong GitHub Personal Access Token (PAT)

Gagamitin ng kursong ito ang GitHub Models Marketplace, na nagbibigay ng libreng access sa Large Language Models (LLMs) na gagamitin mo upang gumawa ng AI Agents.

Upang magamit ang GitHub Models, kailangan mong gumawa ng [GitHub Personal Access Token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens).

Magagawa ito sa pamamagitan ng pagpunta sa iyong <a href="https://github.com/settings/personal-access-tokens" target="_blank">Personal Access Tokens settings</a> sa iyong GitHub Account.

Mangyaring sundin ang [Principle of Least Privilege](https://docs.github.com/en/get-started/learning-to-code/storing-your-secrets-safely) kapag gumagawa ng iyong token. Nangangahulugan ito na dapat mo lamang ibigay ang mga pahintulot na kinakailangan ng token upang patakbuhin ang mga halimbawa ng code sa kursong ito.

1. Piliin ang opsyong `Fine-grained tokens` sa kaliwang bahagi ng iyong screen sa pamamagitan ng pagpunta sa **Developer settings**  
   ![](../../../translated_images/profile_developer_settings.410a859fe749c755c859d414294c5908e307222b2c61819c3203bbeed4470e25.tl.png)

    Pagkatapos, piliin ang `Generate new token`.

    ![Generate Token](../../../translated_images/fga_new_token.1c1a234afe202ab37483944a291ee80c1868e1e78082fd6bd4180fea5d5a15b4.tl.png)

2. Maglagay ng deskriptibong pangalan para sa iyong token na sumasalamin sa layunin nito, upang madali itong makilala sa hinaharap.

    🔐 Rekomendasyon sa Tagal ng Token

    Rekomendadong tagal: 30 araw  
    Para sa mas ligtas na paggamit, maaari kang pumili ng mas maikling panahon—tulad ng 7 araw 🛡️  
    Isang mahusay na paraan upang magtakda ng personal na layunin at tapusin ang kurso habang mataas ang iyong momentum sa pag-aaral 🚀.

    ![Token Name and Expiration](../../../translated_images/token-name-expiry-date.a095fb0de63868640a4c82d6b1bbc92b482930a663917a5983a3c7cd1ef86b77.tl.png)

3. Limitahan ang saklaw ng token sa iyong fork ng repository na ito.

    ![Limit scope to fork repository](../../../translated_images/token_repository_limit.924ade5e11d9d8bb6cd21293987e4579dea860e2ba66d607fb46e49524d53644.tl.png)

4. Higpitan ang mga pahintulot ng token: Sa ilalim ng **Permissions**, i-click ang tab na **Account**, at i-click ang "+ Add permissions" na button. Lalabas ang isang dropdown. Mangyaring hanapin ang **Models** at lagyan ng check ang kahon para dito.  
    ![Add Models Permission](../../../translated_images/add_models_permissions.c0c44ed8b40fc143dc87792da9097d715b7de938354e8f771d65416ecc7816b8.tl.png)

5. I-verify ang mga kinakailangang pahintulot bago gumawa ng token. ![Verify Permissions](../../../translated_images/verify_permissions.06bd9e43987a8b219f171bbcf519e45ababae35b844f5e9757e10afcb619b936.tl.png)

6. Bago gumawa ng token, tiyaking handa kang itago ang token sa isang ligtas na lugar tulad ng password manager vault, dahil hindi na ito ipapakita muli pagkatapos mong likhain ito. ![Store Token Securely](../../../translated_images/store_token_securely.08ee2274c6ad6caf3482f1cd1bad7ca3fdca1ce737bc485bfa6499c84297c789.tl.png)

Kopyahin ang bagong token na iyong ginawa. Idadagdag mo ito ngayon sa iyong `.env` file na kasama sa kursong ito.

### Hakbang 2: Gumawa ng Iyong `.env` File

Upang gumawa ng iyong `.env` file, patakbuhin ang sumusunod na command sa iyong terminal.

```bash
cp .env.example .env
```

Kokopyahin nito ang example file at gagawa ng `.env` sa iyong direktoryo kung saan mo ilalagay ang mga halaga para sa mga environment variable.

Kapag nakopya mo na ang iyong token, buksan ang `.env` file sa iyong paboritong text editor at i-paste ang iyong token sa `GITHUB_TOKEN` field.  
![GitHub Token Field](../../../translated_images/github_token_field.20491ed3224b5f4ab24d10ced7a68c4aba2948fe8999cfc8675edaa16f5e5681.tl.png)

Ngayon ay dapat mo nang mapatakbo ang mga halimbawa ng code sa kursong ito.

## Setup para sa Mga Halimbawa gamit ang Azure AI Foundry at Azure AI Agent Service

### Hakbang 1: Kunin ang Iyong Azure Project Endpoint

Sundin ang mga hakbang sa paggawa ng hub at proyekto sa Azure AI Foundry na matatagpuan dito: [Hub resources overview](https://learn.microsoft.com/en-us/azure/ai-foundry/concepts/ai-resources)

Kapag nagawa mo na ang iyong proyekto, kakailanganin mong kunin ang connection string para sa iyong proyekto.

Magagawa ito sa pamamagitan ng pagpunta sa **Overview** page ng iyong proyekto sa Azure AI Foundry portal.

![Project Connection String](../../../translated_images/project-endpoint.8cf04c9975bbfbf18f6447a599550edb052e52264fb7124d04a12e6175e330a5.tl.png)

### Hakbang 2: Gumawa ng Iyong `.env` File

Upang gumawa ng iyong `.env` file, patakbuhin ang sumusunod na command sa iyong terminal.

```bash
cp .env.example .env
```

Kokopyahin nito ang example file at gagawa ng `.env` sa iyong direktoryo kung saan mo ilalagay ang mga halaga para sa mga environment variable.

Kapag nakopya mo na ang iyong token, buksan ang `.env` file sa iyong paboritong text editor at i-paste ang iyong token sa `PROJECT_ENDPOINT` field.

### Hakbang 3: Mag-sign in sa Azure

Bilang isang security best practice, gagamit tayo ng [keyless authentication](https://learn.microsoft.com/azure/developer/ai/keyless-connections?tabs=csharp%2Cazure-cli?WT.mc_id=academic-105485-koreyst) upang mag-authenticate sa Azure OpenAI gamit ang Microsoft Entra ID.

Susunod, buksan ang terminal at patakbuhin ang `az login --use-device-code` upang mag-sign in sa iyong Azure account.

Kapag naka-log in ka na, piliin ang iyong subscription sa terminal.

## Karagdagang Environment Variables - Azure Search at Azure OpenAI

Para sa Agentic RAG Lesson - Lesson 5 - may mga halimbawa na gumagamit ng Azure Search at Azure OpenAI.

Kung nais mong patakbuhin ang mga halimbawang ito, kakailanganin mong idagdag ang sumusunod na mga environment variable sa iyong `.env` file:

### Overview Page (Project)

- `AZURE_SUBSCRIPTION_ID` - Tingnan ang **Project details** sa **Overview** page ng iyong proyekto.

- `AZURE_AI_PROJECT_NAME` - Tingnan ang itaas ng **Overview** page para sa iyong proyekto.

- `AZURE_OPENAI_SERVICE` - Hanapin ito sa **Included capabilities** tab para sa **Azure OpenAI Service** sa **Overview** page.

### Management Center

- `AZURE_OPENAI_RESOURCE_GROUP` - Pumunta sa **Project properties** sa **Overview** page ng **Management Center**.

- `GLOBAL_LLM_SERVICE` - Sa ilalim ng **Connected resources**, hanapin ang **Azure AI Services** connection name. Kung hindi nakalista, tingnan ang **Azure portal** sa ilalim ng iyong resource group para sa AI Services resource name.

### Models + Endpoints Page

- `AZURE_OPENAI_EMBEDDING_DEPLOYMENT_NAME` - Piliin ang iyong embedding model (hal., `text-embedding-ada-002`) at tandaan ang **Deployment name** mula sa model details.

- `AZURE_OPENAI_CHAT_DEPLOYMENT_NAME` - Piliin ang iyong chat model (hal., `gpt-4o-mini`) at tandaan ang **Deployment name** mula sa model details.

### Azure Portal

- `AZURE_OPENAI_ENDPOINT` - Hanapin ang **Azure AI services**, i-click ito, pagkatapos pumunta sa **Resource Management**, **Keys and Endpoint**, mag-scroll pababa sa "Azure OpenAI endpoints", at kopyahin ang isa na nagsasabing "Language APIs".

- `AZURE_OPENAI_API_KEY` - Mula sa parehong screen, kopyahin ang KEY 1 o KEY 2.

- `AZURE_SEARCH_SERVICE_ENDPOINT` - Hanapin ang iyong **Azure AI Search** resource, i-click ito, at tingnan ang **Overview**.

- `AZURE_SEARCH_API_KEY` - Pagkatapos pumunta sa **Settings** at pagkatapos ay **Keys** upang kopyahin ang primary o secondary admin key.

### External Webpage

- `AZURE_OPENAI_API_VERSION` - Bisitahin ang [API version lifecycle](https://learn.microsoft.com/en-us/azure/ai-services/openai/api-version-deprecation#latest-ga-api-release) page sa ilalim ng **Latest GA API release**.

### Setup keyless authentication

Sa halip na i-hardcode ang iyong mga kredensyal, gagamit tayo ng keyless connection sa Azure OpenAI. Upang gawin ito, mag-i-import tayo ng `DefaultAzureCredential` at tatawagin ang `DefaultAzureCredential` function upang makuha ang kredensyal.

```python
from azure.identity import DefaultAzureCredential, InteractiveBrowserCredential
```

## Nahihirapan?

Kung mayroon kang anumang isyu sa pagpapatakbo ng setup na ito, sumali sa aming <a href="https://discord.gg/kzRShWzttr" target="_blank">Azure AI Community Discord</a> o <a href="https://github.com/microsoft/ai-agents-for-beginners/issues?WT.mc_id=academic-105485-koreyst" target="_blank">gumawa ng isyu</a>.

## Susunod na Aralin

Handa ka nang patakbuhin ang code para sa kursong ito. Masayang pag-aaral tungkol sa mundo ng AI Agents! 

[Introduksyon sa AI Agents at Mga Gamit ng Agent](../01-intro-to-ai-agents/README.md)

---

**Paunawa**:  
Ang dokumentong ito ay isinalin gamit ang AI translation service na [Co-op Translator](https://github.com/Azure/co-op-translator). Bagama't sinisikap naming maging tumpak, pakitandaan na ang mga awtomatikong pagsasalin ay maaaring maglaman ng mga pagkakamali o hindi pagkakatugma. Ang orihinal na dokumento sa kanyang katutubong wika ang dapat ituring na opisyal na pinagmulan. Para sa mahalagang impormasyon, inirerekomenda ang propesyonal na pagsasalin ng tao. Hindi kami mananagot sa anumang hindi pagkakaunawaan o maling interpretasyon na dulot ng paggamit ng pagsasaling ito.