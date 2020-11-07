---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
ms.openlocfilehash: 374263c26a3572e8d85e18d1795c27a761866a4a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744698"
---
# <span data-ttu-id="b7168-101">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b7168-101">Set-AzDataFactoryV2</span></span>

## <span data-ttu-id="b7168-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b7168-102">SYNOPSIS</span></span>
<span data-ttu-id="b7168-103">Skapar en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="b7168-103">Creates a data factory.</span></span>

## <span data-ttu-id="b7168-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b7168-104">SYNTAX</span></span>

### <span data-ttu-id="b7168-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="b7168-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7168-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b7168-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7168-107">ByResourceIdFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="b7168-107">ByResourceIdFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7168-108">ByResourceIdFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="b7168-108">ByResourceIdFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7168-109">ByFactoryNameFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="b7168-109">ByFactoryNameFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7168-110">ByFactoryNameFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="b7168-110">ByFactoryNameFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7168-111">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b7168-111">ByInputObject</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7168-112">ByInputObjectFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="b7168-112">ByInputObjectFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7168-113">ByInputObjectFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="b7168-113">ByInputObjectFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7168-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b7168-114">DESCRIPTION</span></span>
<span data-ttu-id="b7168-115">Cmdleten **set-AzDataFactoryV2** skapar en data fabrik med angivet resurs grupp namn och plats.</span><span class="sxs-lookup"><span data-stu-id="b7168-115">The **Set-AzDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="b7168-116">Utför de här operationerna i följande ordning:--skapa en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="b7168-116">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="b7168-117">--Skapa länkade tjänster.</span><span class="sxs-lookup"><span data-stu-id="b7168-117">-- Create linked services.</span></span>
<span data-ttu-id="b7168-118">--Skapa data uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="b7168-118">-- Create datasets.</span></span>
<span data-ttu-id="b7168-119">--Skapa en rörledning.</span><span class="sxs-lookup"><span data-stu-id="b7168-119">-- Create a pipeline.</span></span>

## <span data-ttu-id="b7168-120">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b7168-120">EXAMPLES</span></span>

### <span data-ttu-id="b7168-121">Exempel 1: skapa en data fabrik</span><span class="sxs-lookup"><span data-stu-id="b7168-121">Example 1: Create a data factory</span></span>
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

### <span data-ttu-id="b7168-122">Exempel 2: skapa en data fabrik med repoconfiguration uppgifter med hjälp av ett befintligt Factory-objekt.</span><span class="sxs-lookup"><span data-stu-id="b7168-122">Example 2: Create a data factory with repoconfiguration details using an existing factory object.</span></span>
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

<span data-ttu-id="b7168-123">Det här kommandot skapar en data fabrik med namnet WikiADF i resurs gruppen med namnet ADF på platsen för västkusten.</span><span class="sxs-lookup"><span data-stu-id="b7168-123">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="b7168-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b7168-124">PARAMETERS</span></span>

### <span data-ttu-id="b7168-125">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b7168-125">-AccountName</span></span>
<span data-ttu-id="b7168-126">Konto namn för repo-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b7168-126">The account name for repo configuration.</span></span>

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

### <span data-ttu-id="b7168-127">-CollaborationBranch</span><span class="sxs-lookup"><span data-stu-id="b7168-127">-CollaborationBranch</span></span>
<span data-ttu-id="b7168-128">Samarbets gren för konfiguration av repo.</span><span class="sxs-lookup"><span data-stu-id="b7168-128">The collaboration branch for repo configuration.</span></span>

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

### <span data-ttu-id="b7168-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7168-129">-DefaultProfile</span></span>
<span data-ttu-id="b7168-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b7168-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7168-131">-Force</span><span class="sxs-lookup"><span data-stu-id="b7168-131">-Force</span></span>
<span data-ttu-id="b7168-132">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="b7168-132">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b7168-133">-HostName</span><span class="sxs-lookup"><span data-stu-id="b7168-133">-HostName</span></span>
<span data-ttu-id="b7168-134">Värd namnet för repo-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b7168-134">The host name for repo configuration.</span></span>

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

### <span data-ttu-id="b7168-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7168-135">-InputObject</span></span>
<span data-ttu-id="b7168-136">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="b7168-136">The data factory object.</span></span>

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

### <span data-ttu-id="b7168-137">-LastCommitId</span><span class="sxs-lookup"><span data-stu-id="b7168-137">-LastCommitId</span></span>
<span data-ttu-id="b7168-138">Senaste bekräftelse-ID för repo-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b7168-138">The last commit id for repo configuration.</span></span>

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

### <span data-ttu-id="b7168-139">-Plats</span><span class="sxs-lookup"><span data-stu-id="b7168-139">-Location</span></span>
<span data-ttu-id="b7168-140">Data fabriken skapas i det här området.</span><span class="sxs-lookup"><span data-stu-id="b7168-140">The data factory is created in this region.</span></span>

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

### <span data-ttu-id="b7168-141">-Namn</span><span class="sxs-lookup"><span data-stu-id="b7168-141">-Name</span></span>
<span data-ttu-id="b7168-142">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="b7168-142">The data factory name.</span></span>

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

### <span data-ttu-id="b7168-143">-Projektetsnamn</span><span class="sxs-lookup"><span data-stu-id="b7168-143">-ProjectName</span></span>
<span data-ttu-id="b7168-144">Projekt namnet för repo-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b7168-144">The project name for repo configuration.</span></span>

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

### <span data-ttu-id="b7168-145">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="b7168-145">-RepositoryName</span></span>
<span data-ttu-id="b7168-146">Databas namnet för repo-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b7168-146">The repository name for repo configuration.</span></span>

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

### <span data-ttu-id="b7168-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7168-147">-ResourceGroupName</span></span>
<span data-ttu-id="b7168-148">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="b7168-148">The resource group name.</span></span>

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

### <span data-ttu-id="b7168-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7168-149">-ResourceId</span></span>
<span data-ttu-id="b7168-150">Azure Resource ID för v2 Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b7168-150">The Azure resource ID of V2 data factory.</span></span>

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

### <span data-ttu-id="b7168-151">-RootFolder</span><span class="sxs-lookup"><span data-stu-id="b7168-151">-RootFolder</span></span>
<span data-ttu-id="b7168-152">Rotmappen för konfiguration av repo.</span><span class="sxs-lookup"><span data-stu-id="b7168-152">The root folder for repo configuration.</span></span>

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

### <span data-ttu-id="b7168-153">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b7168-153">-Tag</span></span>
<span data-ttu-id="b7168-154">Taggarna för data fabriken.</span><span class="sxs-lookup"><span data-stu-id="b7168-154">The tags of the data factory.</span></span>

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

### <span data-ttu-id="b7168-155">-TenantId</span><span class="sxs-lookup"><span data-stu-id="b7168-155">-TenantId</span></span>
<span data-ttu-id="b7168-156">Klient-ID för konfiguration av repo.</span><span class="sxs-lookup"><span data-stu-id="b7168-156">The tenant id for repo configuration.</span></span>

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

### <span data-ttu-id="b7168-157">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b7168-157">-Confirm</span></span>
<span data-ttu-id="b7168-158">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b7168-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7168-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7168-159">-WhatIf</span></span>
<span data-ttu-id="b7168-160">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b7168-160">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="b7168-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7168-161">CommonParameters</span></span>
<span data-ttu-id="b7168-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7168-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7168-163">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7168-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7168-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b7168-164">INPUTS</span></span>

### <span data-ttu-id="b7168-165">System. String</span><span class="sxs-lookup"><span data-stu-id="b7168-165">System.String</span></span>

### <span data-ttu-id="b7168-166">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="b7168-166">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b7168-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b7168-167">OUTPUTS</span></span>

### <span data-ttu-id="b7168-168">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b7168-168">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="b7168-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b7168-169">NOTES</span></span>
<span data-ttu-id="b7168-170">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="b7168-170">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b7168-171">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b7168-171">RELATED LINKS</span></span>

[<span data-ttu-id="b7168-172">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b7168-172">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="b7168-173">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b7168-173">Remove-AzDataFactoryV2</span></span>]()
