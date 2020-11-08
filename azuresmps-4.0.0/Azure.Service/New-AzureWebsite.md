---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FBB55071-454D-4473-93BA-D97F33067785
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f83489d21fba97bb50145de1fedc1ac9a7195a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099414"
---
# <span data-ttu-id="f171c-101">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="f171c-101">New-AzureWebsite</span></span>

## <span data-ttu-id="f171c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f171c-102">SYNOPSIS</span></span>
<span data-ttu-id="f171c-103">Skapa en ny webbplats som ska köras i Azure.</span><span class="sxs-lookup"><span data-stu-id="f171c-103">Create a new website to run in Azure.</span></span>

## <span data-ttu-id="f171c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f171c-104">SYNTAX</span></span>

```
New-AzureWebsite [-Location <String>] [-Hostname <String>] [-PublishingUsername <String>] [-Git] [-GitHub]
 [-GithubCredentials <PSCredential>] [-GithubRepository <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f171c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f171c-105">DESCRIPTION</span></span>
<span data-ttu-id="f171c-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="f171c-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f171c-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="f171c-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f171c-108">Cmdleten skapar en ny webbplats som körs i Azure och förbereder för distribution via GitHub.</span><span class="sxs-lookup"><span data-stu-id="f171c-108">The cmdlet creates a new website to run in Azure and prepares for deployment through Github.</span></span>

## <span data-ttu-id="f171c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f171c-109">EXAMPLES</span></span>

### <span data-ttu-id="f171c-110">Exempel 1: skapa en ny webbplats med git</span><span class="sxs-lookup"><span data-stu-id="f171c-110">Example 1: Create a new website with Git</span></span>
```
PS C:\> New-AzureWebsite mySite -Git
```

<span data-ttu-id="f171c-111">I det här exemplet skapas en ny webbplats i Azure och en lokal Git-databas som används för att distribuera filer till den nya webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="f171c-111">This example creates a new website in Azure and a local Git repository to use for deploying files to the new website.</span></span>

### <span data-ttu-id="f171c-112">Exempel 2: skapa webbplats integrerad med GitHub</span><span class="sxs-lookup"><span data-stu-id="f171c-112">Example 2: Create website integrated with Github</span></span>
```
PS C:\> New-AzureWebsite mysite -Github -GithubRepository myaccount/myrepo
```

<span data-ttu-id="f171c-113">I det här exemplet skapas en ny webbplats som är länkad till en GitHub-databas som heter myrepo.</span><span class="sxs-lookup"><span data-stu-id="f171c-113">This example creates a new website linked to a Github repository named myaccount/myrepo.</span></span>
<span data-ttu-id="f171c-114">Sparar till GitHub-databasen skickas till webbplatsen i Azure.</span><span class="sxs-lookup"><span data-stu-id="f171c-114">Commits to the Github repository are pushed to the website in Azure.</span></span>

## <span data-ttu-id="f171c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f171c-115">PARAMETERS</span></span>

### <span data-ttu-id="f171c-116">-Git</span><span class="sxs-lookup"><span data-stu-id="f171c-116">-Git</span></span>
<span data-ttu-id="f171c-117">Konfigurerar en lokal Git-databas och länkar den till webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="f171c-117">Sets up a local Git repository and links it to the website.</span></span>
<span data-ttu-id="f171c-118">Om det här alternativet anges konfigurerar den här parametern en Git-databas i den lokala katalogen och lägger till en fjärrdatabas med namnet "Azure" som länkar till webbplatsen i Azure.</span><span class="sxs-lookup"><span data-stu-id="f171c-118">If specified, this parameter sets up a Git repository in the local directory and add a remote repository named 'azure' that links to the website in Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f171c-119">-GitHub</span><span class="sxs-lookup"><span data-stu-id="f171c-119">-GitHub</span></span>
<span data-ttu-id="f171c-120">Anger att den här cmdleten länkar den nya webbplatsen till en befintlig GitHub-databas.</span><span class="sxs-lookup"><span data-stu-id="f171c-120">Indicates that this cmdlet links the new website to an existing Github repository.</span></span>
<span data-ttu-id="f171c-121">Sparar till Giuthub-databasen skickas till webbplatsen i Azure.</span><span class="sxs-lookup"><span data-stu-id="f171c-121">Commits to the Giuthub repository are pushed to the website in Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f171c-122">-GithubCredentials</span><span class="sxs-lookup"><span data-stu-id="f171c-122">-GithubCredentials</span></span>
<span data-ttu-id="f171c-123">Anger användar namn och lösen ords uppgifter för att ansluta till GitHub.</span><span class="sxs-lookup"><span data-stu-id="f171c-123">Specifies the user name and password credentials to connect to Github.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f171c-124">-GithubRepository</span><span class="sxs-lookup"><span data-stu-id="f171c-124">-GithubRepository</span></span>
<span data-ttu-id="f171c-125">Anger det fullständiga namnet på den GitHub-databas som du vill länka till webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="f171c-125">Specifies the full name of the Github repository to link to this website.</span></span>
<span data-ttu-id="f171c-126">Till exempel `myaccount/myrepo` .</span><span class="sxs-lookup"><span data-stu-id="f171c-126">For example, `myaccount/myrepo`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f171c-127">-Hostname</span><span class="sxs-lookup"><span data-stu-id="f171c-127">-Hostname</span></span>
<span data-ttu-id="f171c-128">Anger ett alternativt värdnamn för den nya webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="f171c-128">Specifies an alternative host name for the new website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f171c-129">-Plats</span><span class="sxs-lookup"><span data-stu-id="f171c-129">-Location</span></span>
<span data-ttu-id="f171c-130">Anger platsen för det data Center som du vill distribuera webbplatsen till.</span><span class="sxs-lookup"><span data-stu-id="f171c-130">Specifies the location of the data center where you want to deploy the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f171c-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="f171c-131">-Name</span></span>
<span data-ttu-id="f171c-132">Anger ett namn för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="f171c-132">Specifies a name for the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f171c-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="f171c-133">-Profile</span></span>
<span data-ttu-id="f171c-134">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="f171c-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f171c-135">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="f171c-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f171c-136">-PublishingUsername</span><span class="sxs-lookup"><span data-stu-id="f171c-136">-PublishingUsername</span></span>
<span data-ttu-id="f171c-137">Anger det användar namn som du har angett i Azure-portalen för Git-distribution.</span><span class="sxs-lookup"><span data-stu-id="f171c-137">Specifies the user name you have specified in the Azure Portal for Git deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f171c-138">-Plats</span><span class="sxs-lookup"><span data-stu-id="f171c-138">-Slot</span></span>
<span data-ttu-id="f171c-139">Anger ett plats namn för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="f171c-139">Specifies a slot name for the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f171c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f171c-140">CommonParameters</span></span>
<span data-ttu-id="f171c-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f171c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f171c-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f171c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f171c-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f171c-143">INPUTS</span></span>

## <span data-ttu-id="f171c-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f171c-144">OUTPUTS</span></span>

## <span data-ttu-id="f171c-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f171c-145">NOTES</span></span>

## <span data-ttu-id="f171c-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f171c-146">RELATED LINKS</span></span>

[<span data-ttu-id="f171c-147">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="f171c-147">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


