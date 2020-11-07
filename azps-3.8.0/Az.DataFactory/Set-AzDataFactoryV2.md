---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
ms.openlocfilehash: 219e5b18a04332d2ee840fb41b92aa9d282a1792
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927741"
---
# <span data-ttu-id="9840b-101">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="9840b-101">Set-AzDataFactoryV2</span></span>

## <span data-ttu-id="9840b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9840b-102">SYNOPSIS</span></span>
<span data-ttu-id="9840b-103">Skapar en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="9840b-103">Creates a data factory.</span></span>

## <span data-ttu-id="9840b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9840b-104">SYNTAX</span></span>

### <span data-ttu-id="9840b-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="9840b-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9840b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9840b-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9840b-107">ByResourceIdFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="9840b-107">ByResourceIdFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9840b-108">ByResourceIdFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="9840b-108">ByResourceIdFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9840b-109">ByFactoryNameFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="9840b-109">ByFactoryNameFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9840b-110">ByFactoryNameFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="9840b-110">ByFactoryNameFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9840b-111">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9840b-111">ByInputObject</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9840b-112">ByInputObjectFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="9840b-112">ByInputObjectFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9840b-113">ByInputObjectFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="9840b-113">ByInputObjectFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9840b-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9840b-114">DESCRIPTION</span></span>
<span data-ttu-id="9840b-115">Cmdleten **set-AzDataFactoryV2** skapar en data fabrik med angivet resurs grupp namn och plats.</span><span class="sxs-lookup"><span data-stu-id="9840b-115">The **Set-AzDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="9840b-116">Utför de här operationerna i följande ordning:--skapa en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="9840b-116">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="9840b-117">--Skapa länkade tjänster.</span><span class="sxs-lookup"><span data-stu-id="9840b-117">-- Create linked services.</span></span>
<span data-ttu-id="9840b-118">--Skapa data uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="9840b-118">-- Create datasets.</span></span>
<span data-ttu-id="9840b-119">--Skapa en rörledning.</span><span class="sxs-lookup"><span data-stu-id="9840b-119">-- Create a pipeline.</span></span>

## <span data-ttu-id="9840b-120">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9840b-120">EXAMPLES</span></span>

### <span data-ttu-id="9840b-121">Exempel 1: skapa en data fabrik</span><span class="sxs-lookup"><span data-stu-id="9840b-121">Example 1: Create a data factory</span></span>
```
PS C:\> Set-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
    RepoConfiguration :
```

### <span data-ttu-id="9840b-122">Exempel 2: skapa en data fabrik med repo med hjälp av ett befintligt Factory-objekt.</span><span class="sxs-lookup"><span data-stu-id="9840b-122">Example 2: Create a data factory with repo configuration details using an existing factory object.</span></span>
```
PS C:\> Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" | Set-AzDataFactoryV2 -AccountName msdata -RepositoryName ADFRepo -CollaborationBranch master -RootFolder / -ProjectName "Azure Data Factory"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
    RepoConfiguration : Microsoft.Azure.Management.DataFactory.Models.FactoryVSTSConfiguration
```

<span data-ttu-id="9840b-123">Det här kommandot skapar en data fabrik med namnet WikiADF i resurs gruppen med namnet ADF på platsen med Azure DevOps Source Control.</span><span class="sxs-lookup"><span data-stu-id="9840b-123">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with Azure DevOps source control configuration.</span></span>

### <span data-ttu-id="9840b-124">Exempel 3: skapa en data fabrik med GitHub repo konfigurations uppgifter med hjälp av ett nytt fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="9840b-124">Example 3: Create a data factory with GitHub repo configuration details using a new factory object.</span></span>
```
PS C:\> New-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Location 'EastUS' -HostName 'https://github.com' -AccountName msdata -RepositoryName ADFRepo -CollaborationBranch master -RootFolder /

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
    RepoConfiguration : Microsoft.Azure.Management.DataFactory.Models.FactoryGitHubConfiguration
```

<span data-ttu-id="9840b-125">Det här kommandot skapar en data fabrik med namnet WikiADF i resurs gruppen med namnet ADF på platsen med GitHub-käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="9840b-125">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with GitHub source control configuration..</span></span>

## <span data-ttu-id="9840b-126">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9840b-126">PARAMETERS</span></span>

### <span data-ttu-id="9840b-127">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9840b-127">-AccountName</span></span>
<span data-ttu-id="9840b-128">Konto namn för repo-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9840b-128">The account name for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9840b-129">-CollaborationBranch</span><span class="sxs-lookup"><span data-stu-id="9840b-129">-CollaborationBranch</span></span>
<span data-ttu-id="9840b-130">Samarbets gren för konfiguration av repo.</span><span class="sxs-lookup"><span data-stu-id="9840b-130">The collaboration branch for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9840b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9840b-131">-DefaultProfile</span></span>
<span data-ttu-id="9840b-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9840b-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9840b-133">-Force</span><span class="sxs-lookup"><span data-stu-id="9840b-133">-Force</span></span>
<span data-ttu-id="9840b-134">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="9840b-134">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9840b-135">-HostName</span><span class="sxs-lookup"><span data-stu-id="9840b-135">-HostName</span></span>
<span data-ttu-id="9840b-136">Värd namnet för GitHub repo-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9840b-136">The host name for GitHub repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9840b-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9840b-137">-InputObject</span></span>
<span data-ttu-id="9840b-138">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="9840b-138">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByInputObject, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9840b-139">-LastCommitId</span><span class="sxs-lookup"><span data-stu-id="9840b-139">-LastCommitId</span></span>
<span data-ttu-id="9840b-140">Senaste bekräftelse-ID för repo-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9840b-140">The last commit id for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9840b-141">-Plats</span><span class="sxs-lookup"><span data-stu-id="9840b-141">-Location</span></span>
<span data-ttu-id="9840b-142">Data fabriken skapas i det här området.</span><span class="sxs-lookup"><span data-stu-id="9840b-142">The data factory is created in this region.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByResourceId, ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9840b-143">-Namn</span><span class="sxs-lookup"><span data-stu-id="9840b-143">-Name</span></span>
<span data-ttu-id="9840b-144">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="9840b-144">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9840b-145">-Projektetsnamn</span><span class="sxs-lookup"><span data-stu-id="9840b-145">-ProjectName</span></span>
<span data-ttu-id="9840b-146">Project-DevOps för repo-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9840b-146">The project name Azure DevOps for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByFactoryNameFactoryRepoVstsConfig, ByInputObjectFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9840b-147">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="9840b-147">-RepositoryName</span></span>
<span data-ttu-id="9840b-148">Databas namnet för repo-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9840b-148">The repository name for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9840b-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9840b-149">-ResourceGroupName</span></span>
<span data-ttu-id="9840b-150">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="9840b-150">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9840b-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9840b-151">-ResourceId</span></span>
<span data-ttu-id="9840b-152">Azure Resource ID för v2 Data Factory.</span><span class="sxs-lookup"><span data-stu-id="9840b-152">The Azure resource ID of V2 data factory.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId, ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig
Aliases: Id, DataFactoryId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9840b-153">-RootFolder</span><span class="sxs-lookup"><span data-stu-id="9840b-153">-RootFolder</span></span>
<span data-ttu-id="9840b-154">Rotmappen för konfiguration av repo.</span><span class="sxs-lookup"><span data-stu-id="9840b-154">The root folder for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9840b-155">-Tagg</span><span class="sxs-lookup"><span data-stu-id="9840b-155">-Tag</span></span>
<span data-ttu-id="9840b-156">Taggarna för data fabriken.</span><span class="sxs-lookup"><span data-stu-id="9840b-156">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFactoryName, ByResourceId, ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByInputObject, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9840b-157">-TenantId</span><span class="sxs-lookup"><span data-stu-id="9840b-157">-TenantId</span></span>
<span data-ttu-id="9840b-158">Klient-ID för Azure DevOps repo-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9840b-158">The tenant id for Azure DevOps repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByFactoryNameFactoryRepoVstsConfig, ByInputObjectFactoryRepoVstsConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9840b-159">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9840b-159">-Confirm</span></span>
<span data-ttu-id="9840b-160">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9840b-160">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9840b-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9840b-161">-WhatIf</span></span>
<span data-ttu-id="9840b-162">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9840b-162">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9840b-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9840b-163">CommonParameters</span></span>
<span data-ttu-id="9840b-164">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9840b-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9840b-165">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9840b-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9840b-166">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9840b-166">INPUTS</span></span>

### <span data-ttu-id="9840b-167">System. String</span><span class="sxs-lookup"><span data-stu-id="9840b-167">System.String</span></span>

### <span data-ttu-id="9840b-168">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="9840b-168">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9840b-169">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9840b-169">OUTPUTS</span></span>

### <span data-ttu-id="9840b-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9840b-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="9840b-171">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9840b-171">NOTES</span></span>
<span data-ttu-id="9840b-172">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="9840b-172">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9840b-173">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9840b-173">RELATED LINKS</span></span>

[<span data-ttu-id="9840b-174">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="9840b-174">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="9840b-175">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="9840b-175">Remove-AzDataFactoryV2</span></span>]()
