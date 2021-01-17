---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 87c3f0e2e86f2867d659b26b5acc9df5a6dfe8c7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419824"
---
# <span data-ttu-id="c38b0-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="c38b0-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="c38b0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c38b0-102">SYNOPSIS</span></span>
<span data-ttu-id="c38b0-103">Ställer in avancerade inställningar för skydd mot SQL-pooler.</span><span class="sxs-lookup"><span data-stu-id="c38b0-103">Sets a advanced threat protection settings on a SQL pool.</span></span>

## <span data-ttu-id="c38b0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c38b0-104">SYNTAX</span></span>

### <span data-ttu-id="c38b0-105">UpdateByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c38b0-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>]
 [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c38b0-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c38b0-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c38b0-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c38b0-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c38b0-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c38b0-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c38b0-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c38b0-109">DESCRIPTION</span></span>
<span data-ttu-id="c38b0-110">Cmdleten **Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting** anger ett avancerat skydds inställningar för en Azure SYNAPSE Analytics SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="c38b0-110">The **Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure Synapse Analytics SQL pool.</span></span>
<span data-ttu-id="c38b0-111">För att aktivera avancerat skydd för en SQL-pool måste gransknings inställningarna vara aktiverade på den SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="c38b0-111">In order to enable advanced threat protection on a SQL pool an auditing settings must be enabled on that SQL pool.</span></span>

## <span data-ttu-id="c38b0-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c38b0-112">EXAMPLES</span></span>

### <span data-ttu-id="c38b0-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c38b0-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="c38b0-114">Det här kommandot anger de avancerade inställningarna för skydd mot en SQL-pool som heter ContosoSqlPool under arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="c38b0-114">This command sets the advanced threat protection settings for a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="c38b0-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c38b0-115">PARAMETERS</span></span>

### <span data-ttu-id="c38b0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c38b0-116">-AsJob</span></span>
<span data-ttu-id="c38b0-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="c38b0-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c38b0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c38b0-118">-DefaultProfile</span></span>
<span data-ttu-id="c38b0-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c38b0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c38b0-120">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="c38b0-120">-EmailAdmin</span></span>
<span data-ttu-id="c38b0-121">Anger om du vill skicka e-postadministratörer.</span><span class="sxs-lookup"><span data-stu-id="c38b0-121">Defines whether to email administrators.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: EmailAdmins

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c38b0-122">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="c38b0-122">-ExcludedDetectionType</span></span>
<span data-ttu-id="c38b0-123">Identifierings typer som ska undantas.</span><span class="sxs-lookup"><span data-stu-id="c38b0-123">Detection types to exclude.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c38b0-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c38b0-124">-InputObject</span></span>
<span data-ttu-id="c38b0-125">Objekt i SQL-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="c38b0-125">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c38b0-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="c38b0-126">-Name</span></span>
<span data-ttu-id="c38b0-127">Namn på SQL-poolen Synapse.</span><span class="sxs-lookup"><span data-stu-id="c38b0-127">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c38b0-128">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="c38b0-128">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="c38b0-129">En semikolonavgränsad lista med e-postadresser som aviseringar skickas till.</span><span class="sxs-lookup"><span data-stu-id="c38b0-129">A semicolon separated list of email addresses to send the alerts to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NotificationRecipientsEmails

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c38b0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c38b0-130">-ResourceGroupName</span></span>
<span data-ttu-id="c38b0-131">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="c38b0-131">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c38b0-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c38b0-132">-ResourceId</span></span>
<span data-ttu-id="c38b0-133">Resurs-ID för Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="c38b0-133">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c38b0-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="c38b0-134">-RetentionInDays</span></span>
<span data-ttu-id="c38b0-135">Antalet bevarande dagar för gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="c38b0-135">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c38b0-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c38b0-136">-StorageAccountName</span></span>
<span data-ttu-id="c38b0-137">Namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="c38b0-137">The name of the storage account.</span></span>

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

### <span data-ttu-id="c38b0-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c38b0-138">-WorkspaceName</span></span>
<span data-ttu-id="c38b0-139">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="c38b0-139">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c38b0-140">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c38b0-140">-WorkspaceObject</span></span>
<span data-ttu-id="c38b0-141">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="c38b0-141">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c38b0-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c38b0-142">-Confirm</span></span>
<span data-ttu-id="c38b0-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c38b0-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c38b0-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c38b0-144">-WhatIf</span></span>
<span data-ttu-id="c38b0-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c38b0-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c38b0-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c38b0-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c38b0-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c38b0-147">CommonParameters</span></span>
<span data-ttu-id="c38b0-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c38b0-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c38b0-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c38b0-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c38b0-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c38b0-150">INPUTS</span></span>

### <span data-ttu-id="c38b0-151">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c38b0-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="c38b0-152">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="c38b0-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="c38b0-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c38b0-153">OUTPUTS</span></span>

### <span data-ttu-id="c38b0-154">Microsoft. Azure. commands. Synapse. Models. PSSqlPoolSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="c38b0-154">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span></span>

## <span data-ttu-id="c38b0-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c38b0-155">NOTES</span></span>

## <span data-ttu-id="c38b0-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c38b0-156">RELATED LINKS</span></span>
