---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 4fb27d1d822d72de9564e9acc900122016940c6d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419832"
---
# <span data-ttu-id="448fa-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="448fa-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="448fa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="448fa-102">SYNOPSIS</span></span>
<span data-ttu-id="448fa-103">Uppdaterar ett avancerat skydd på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="448fa-103">Updates an advanced threat protection settings on a workspace.</span></span>

## <span data-ttu-id="448fa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="448fa-104">SYNTAX</span></span>

### <span data-ttu-id="448fa-105">UpdateByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="448fa-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="448fa-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="448fa-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="448fa-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="448fa-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-NotificationRecipientsEmail <String>]
 [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="448fa-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="448fa-108">DESCRIPTION</span></span>
<span data-ttu-id="448fa-109">Cmdleten **Update-AzSynapseSqlAdvancedThreatProtectionSetting** uppdaterar ett avancerat skydds inställningar på en Azure Synapse Analytics-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="448fa-109">The **Update-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet updates an advanced threat protection settings on an Azure Synapse Analytics Workspace.</span></span> <span data-ttu-id="448fa-110">För att aktivera avancerat skydd för en arbets yta måste gransknings inställningar vara aktiverade på den arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="448fa-110">In order to enable advanced threat protection on a workspace an auditing settings must be enabled on that workspace.</span></span>

## <span data-ttu-id="448fa-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="448fa-111">EXAMPLES</span></span>

### <span data-ttu-id="448fa-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="448fa-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -NotificationRecipientsEmail "admin01@contoso.com;secadmin@contoso.com" -EmailAdmin $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="448fa-113">Det här kommandot uppdaterar inställningarna för avancerat skydd för en arbets yta med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="448fa-113">This command updates the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="448fa-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="448fa-114">PARAMETERS</span></span>

### <span data-ttu-id="448fa-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="448fa-115">-AsJob</span></span>
<span data-ttu-id="448fa-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="448fa-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="448fa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="448fa-117">-DefaultProfile</span></span>
<span data-ttu-id="448fa-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="448fa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="448fa-119">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="448fa-119">-EmailAdmin</span></span>
<span data-ttu-id="448fa-120">Anger om du vill skicka e-postadministratörer.</span><span class="sxs-lookup"><span data-stu-id="448fa-120">Defines whether to email administrators.</span></span>

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

### <span data-ttu-id="448fa-121">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="448fa-121">-ExcludedDetectionType</span></span>
<span data-ttu-id="448fa-122">Identifierings typer som ska undantas.</span><span class="sxs-lookup"><span data-stu-id="448fa-122">Detection types to exclude.</span></span>

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

### <span data-ttu-id="448fa-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="448fa-123">-InputObject</span></span>
<span data-ttu-id="448fa-124">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="448fa-124">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="448fa-125">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="448fa-125">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="448fa-126">En semikolonavgränsad lista med e-postadresser som aviseringar skickas till.</span><span class="sxs-lookup"><span data-stu-id="448fa-126">A semicolon separated list of email addresses to send the alerts to.</span></span>

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

### <span data-ttu-id="448fa-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="448fa-127">-ResourceGroupName</span></span>
<span data-ttu-id="448fa-128">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="448fa-128">Resource group name.</span></span>

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

### <span data-ttu-id="448fa-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="448fa-129">-ResourceId</span></span>
<span data-ttu-id="448fa-130">Resurs-ID för Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="448fa-130">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="448fa-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="448fa-131">-RetentionInDays</span></span>
<span data-ttu-id="448fa-132">Antalet bevarande dagar för gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="448fa-132">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="448fa-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="448fa-133">-StorageAccountName</span></span>
<span data-ttu-id="448fa-134">Namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="448fa-134">The name of the storage account.</span></span>

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

### <span data-ttu-id="448fa-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="448fa-135">-WorkspaceName</span></span>
<span data-ttu-id="448fa-136">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="448fa-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="448fa-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="448fa-137">-Confirm</span></span>
<span data-ttu-id="448fa-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="448fa-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="448fa-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="448fa-139">-WhatIf</span></span>
<span data-ttu-id="448fa-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="448fa-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="448fa-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="448fa-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="448fa-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="448fa-142">CommonParameters</span></span>
<span data-ttu-id="448fa-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="448fa-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="448fa-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="448fa-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="448fa-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="448fa-145">INPUTS</span></span>

### <span data-ttu-id="448fa-146">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="448fa-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="448fa-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="448fa-147">OUTPUTS</span></span>

### <span data-ttu-id="448fa-148">Microsoft. Azure. commands. Synapse. Models. PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="448fa-148">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="448fa-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="448fa-149">NOTES</span></span>

## <span data-ttu-id="448fa-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="448fa-150">RELATED LINKS</span></span>
