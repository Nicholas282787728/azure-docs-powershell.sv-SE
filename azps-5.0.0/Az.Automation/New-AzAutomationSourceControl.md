---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
ms.openlocfilehash: 17d1c7c94726543aa30a032423576c8a7dcb6fcc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321859"
---
# <span data-ttu-id="7e6cf-101">New-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="7e6cf-101">New-AzAutomationSourceControl</span></span>

## <span data-ttu-id="7e6cf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7e6cf-102">SYNOPSIS</span></span>
<span data-ttu-id="7e6cf-103">Skapar en kontroll för en automatiserings källa.</span><span class="sxs-lookup"><span data-stu-id="7e6cf-103">Creates an A Automation source control.</span></span>

## <span data-ttu-id="7e6cf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7e6cf-104">SYNTAX</span></span>

```
New-AzAutomationSourceControl -Name <String> -RepoUrl <Uri> -SourceType <String> -AccessToken <SecureString>
 -FolderPath <String> [-Branch <String>] [-Description <String>] [-EnableAutoSync] [-DoNotPublishRunbook]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e6cf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7e6cf-105">DESCRIPTION</span></span>
<span data-ttu-id="7e6cf-106">New-AzAutomationSourceControl-cmdleten skapar en konfiguration för att länka mitt Azure Automation-konto med My VSTS TFVC, VSTS git eller GitHub.</span><span class="sxs-lookup"><span data-stu-id="7e6cf-106">The New-AzAutomationSourceControl cmdlet creates a configuration to link my Azure Automation account with my VSTS TFVC, VSTS Git or GitHub.</span></span>

## <span data-ttu-id="7e6cf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7e6cf-107">EXAMPLES</span></span>

### <span data-ttu-id="7e6cf-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7e6cf-108">Example 1</span></span>
<span data-ttu-id="7e6cf-109">Skapa en käll kontroll konfiguration för att länka mitt Azure Automation-konto med mitt VSTS TFVC-projekt.</span><span class="sxs-lookup"><span data-stu-id="7e6cf-109">Create a source control configuration to link my Azure Automation account with my VSTS TFVC project.</span></span> <span data-ttu-id="7e6cf-110">TFVC-projekt har ingen förgrening och därför anges inte parametern Branch.</span><span class="sxs-lookup"><span data-stu-id="7e6cf-110">TFVC projects do not have branches, and therefore, the Branch parameter is not specified.</span></span>

```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSNative" `
                                           -RepoUrl "https://contoso.visualstudio.com/ContosoProduction/_versionControl" `
                                           -SourceType "VsoTfvc" `
                                           -FolderPath "/Runbooks" `
                                           -AccessToken $accessToken

Name        SourceType Branch FolderPath AutoSync PublishRunbook RepoUrl
----        ---------- ------ ---------- -------- -------------- -------
VSTSNative  VsoTfvc            /Runbooks True     True           https://contoso.visualstudio.com/ContosoProduc...
```

### <span data-ttu-id="7e6cf-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7e6cf-111">Example 2</span></span>
<span data-ttu-id="7e6cf-112">Skapa en käll kontroll konfiguration för att länka mitt Azure Automation-konto med mitt VSTS git-projekt.</span><span class="sxs-lookup"><span data-stu-id="7e6cf-112">Create a source control configuration to link my Azure Automation account with my VSTS Git project.</span></span>


```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSGit" `
                                           -RepoUrl "https://contoso.visualstudio.com/_git/Finance" `
                                           -SourceType "VsoGit" `
                                           -Branch "Development" `
                                           -FolderPath "/" `
                                           -AccessToken $accessToken

Name    SourceType Branch      FolderPath AutoSync PublishRunbook RepoUrl
----    ---------- ------      ---------- -------- -------------- -------
VSTSGit VsoGit     Development /          True     True           https://contoso.visualstudio.com/_git/Finan...
```

### <span data-ttu-id="7e6cf-113">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="7e6cf-113">Example 3</span></span>
<span data-ttu-id="7e6cf-114">Skapa en käll kontroll konfiguration för att länka mitt Azure Automation-konto med mitt GitHub-projekt.</span><span class="sxs-lookup"><span data-stu-id="7e6cf-114">Create a source control configuration to link my Azure Automation account with my GitHub project.</span></span>


```powershell
PS C:\> # GitHub access token
PS C:\> $token = "68b08011223aac8bdd3388913a44rrsaa84fdf"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "GitHub1" `
                                           -RepoUrl "https://github.com/Contoso/TestSourceControl.git" `
                                           -SourceType "GitHub" `
                                           -Branch "master" `
                                           -FolderPath "/Runbooks" `
                                           -AccessToken $accessToken

Name    SourceType Branch FolderPath AutoSync PublishRunbook RepoUrl
----    ---------- ------ ---------- -------- -------------- -------
GitHub1 GitHub     master /Runbooks  True     True           https://github.com/Contoso/TestSourceControl...
```

## <span data-ttu-id="7e6cf-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7e6cf-115">PARAMETERS</span></span>

### <span data-ttu-id="7e6cf-116">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="7e6cf-116">-AccessToken</span></span>
<span data-ttu-id="7e6cf-117">Åtkomst till käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="7e6cf-117">The source control access token.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e6cf-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7e6cf-118">-AutomationAccountName</span></span>
<span data-ttu-id="7e6cf-119">Namnet på Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="7e6cf-119">The automation account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e6cf-120">-Gren</span><span class="sxs-lookup"><span data-stu-id="7e6cf-120">-Branch</span></span>
<span data-ttu-id="7e6cf-121">Käll kontrolls grenen.</span><span class="sxs-lookup"><span data-stu-id="7e6cf-121">The source control branch.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e6cf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e6cf-122">-DefaultProfile</span></span>
<span data-ttu-id="7e6cf-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7e6cf-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e6cf-124">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="7e6cf-124">-Description</span></span>
<span data-ttu-id="7e6cf-125">Käll kontroll beskrivningen.</span><span class="sxs-lookup"><span data-stu-id="7e6cf-125">The source control description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e6cf-126">-DoNotPublishRunbook</span><span class="sxs-lookup"><span data-stu-id="7e6cf-126">-DoNotPublishRunbook</span></span>
<span data-ttu-id="7e6cf-127">Egenskapen publishRunbook för käll kontrollen.</span><span class="sxs-lookup"><span data-stu-id="7e6cf-127">The publishRunbook property of the source control.</span></span>
<span data-ttu-id="7e6cf-128">Om DoNotPublishRunbook är aktive rad innebär det att användare Runbooks importeras som "utkast".</span><span class="sxs-lookup"><span data-stu-id="7e6cf-128">If DoNotPublishRunbook is set, this means that user runbooks will be imported as 'Draft'.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e6cf-129">-EnableAutoSync</span><span class="sxs-lookup"><span data-stu-id="7e6cf-129">-EnableAutoSync</span></span>
<span data-ttu-id="7e6cf-130">Egenskapen AutoSync för käll kontrollen.</span><span class="sxs-lookup"><span data-stu-id="7e6cf-130">The autoSync property for the source control.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e6cf-131">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="7e6cf-131">-FolderPath</span></span>
<span data-ttu-id="7e6cf-132">Sökvägen till käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="7e6cf-132">The source control folder path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e6cf-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="7e6cf-133">-Name</span></span>
<span data-ttu-id="7e6cf-134">Namn på käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="7e6cf-134">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e6cf-135">-Omhäll</span><span class="sxs-lookup"><span data-stu-id="7e6cf-135">-RepoUrl</span></span>
<span data-ttu-id="7e6cf-136">Käll kontrollens repo-URL.</span><span class="sxs-lookup"><span data-stu-id="7e6cf-136">The source control repo url.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e6cf-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e6cf-137">-ResourceGroupName</span></span>
<span data-ttu-id="7e6cf-138">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="7e6cf-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e6cf-139">-SourceType</span><span class="sxs-lookup"><span data-stu-id="7e6cf-139">-SourceType</span></span>
<span data-ttu-id="7e6cf-140">Käll kontroll typen.</span><span class="sxs-lookup"><span data-stu-id="7e6cf-140">The source control type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GitHub, VsoGit, VsoTfvc

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e6cf-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7e6cf-141">-Confirm</span></span>
<span data-ttu-id="7e6cf-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7e6cf-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e6cf-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e6cf-143">-WhatIf</span></span>
<span data-ttu-id="7e6cf-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7e6cf-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e6cf-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7e6cf-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e6cf-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e6cf-146">CommonParameters</span></span>
<span data-ttu-id="7e6cf-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e6cf-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e6cf-148">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e6cf-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e6cf-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7e6cf-149">INPUTS</span></span>

### <span data-ttu-id="7e6cf-150">System. String</span><span class="sxs-lookup"><span data-stu-id="7e6cf-150">System.String</span></span>

## <span data-ttu-id="7e6cf-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7e6cf-151">OUTPUTS</span></span>

### <span data-ttu-id="7e6cf-152">Microsoft. Azure. commands. Automation. Model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="7e6cf-152">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="7e6cf-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7e6cf-153">NOTES</span></span>

## <span data-ttu-id="7e6cf-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7e6cf-154">RELATED LINKS</span></span>
