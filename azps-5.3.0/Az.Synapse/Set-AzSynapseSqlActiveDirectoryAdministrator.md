---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: 4a2293384cdf2cf579458d05c112469d096bfd9a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523908"
---
# <span data-ttu-id="3f2ec-101">Set-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="3f2ec-101">Set-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="3f2ec-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f2ec-102">SYNOPSIS</span></span>
<span data-ttu-id="3f2ec-103">Etablerar en Azure AD-administratör för Synapse Analytics SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-103">Provisions an Azure AD administrator for Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="3f2ec-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f2ec-104">SYNTAX</span></span>

### <span data-ttu-id="3f2ec-105">SetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3f2ec-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 -DisplayName <String> [-ObjectId <Guid>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f2ec-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f2ec-106">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace> -DisplayName <String>
 [-ObjectId <Guid>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f2ec-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f2ec-107">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> -DisplayName <String> [-ObjectId <Guid>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f2ec-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f2ec-108">DESCRIPTION</span></span>
<span data-ttu-id="3f2ec-109">Cmdleten **set-AzSynapseSqlActiveDirectoryAdministrator** etablerar en Azure AD-administratör för Azure Synapse Analytics-arbets ytan i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-109">The **Set-AzSynapseSqlActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for Azure Synapse Analytics Workspace in the current subscription.</span></span>
<span data-ttu-id="3f2ec-110">Du kan endast etablera en administratör åt gången.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-110">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="3f2ec-111">Följande medlemmar i Azure AD kan etableras som en Synapse-administratör för Analytics-arbets yta:</span><span class="sxs-lookup"><span data-stu-id="3f2ec-111">The following members of Azure AD can be provisioned as a Synapse Analytics Workspace administrator:</span></span>
- <span data-ttu-id="3f2ec-112">Egna medlemmar i Azure AD</span><span class="sxs-lookup"><span data-stu-id="3f2ec-112">Native members of Azure AD</span></span> 
- <span data-ttu-id="3f2ec-113">Sammanslagna medlemmar i Azure AD</span><span class="sxs-lookup"><span data-stu-id="3f2ec-113">Federated members of Azure AD</span></span> 
- <span data-ttu-id="3f2ec-114">Importerade medlemmar från andra Azure-annonser som är egna eller sammanlänkade medlemmar</span><span class="sxs-lookup"><span data-stu-id="3f2ec-114">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="3f2ec-115">Azure AD-grupper som har skapats som säkerhets grupper Microsoft-konton, till exempel dem i Outlook.com-, Hotmail.com-eller Live.com-domäner, stöds inte som administratörer.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-115">Azure AD groups created as security groups Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="3f2ec-116">Andra gäst konton, till exempel dem i Gmail.com-eller Yahoo.com-domänerna, stöds inte som administratörer.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-116">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="3f2ec-117">Vi rekommenderar att du tillhandahåller en dedikerad Azure AD-grupp som administratör.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-117">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="3f2ec-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f2ec-118">EXAMPLES</span></span>

### <span data-ttu-id="3f2ec-119">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3f2ec-119">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace -DisplayName "DBAs"
```

<span data-ttu-id="3f2ec-120">Det här kommandot etablerar en Azure AD-administratörs grupp med namnet DBAs för arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-120">This command provisions an Azure AD administrator group named DBAs for the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="3f2ec-121">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="3f2ec-121">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
```

<span data-ttu-id="3f2ec-122">Det här kommandot etablerar en Azure AD-administratörs grupp med namnet DBAs för arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-122">This command provisions an Azure AD administrator group named DBAs for the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="3f2ec-123">Det gör att kommandot fungerar även om gruppens visnings namn inte är unikt.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-123">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="3f2ec-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f2ec-124">PARAMETERS</span></span>

### <span data-ttu-id="3f2ec-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f2ec-125">-AsJob</span></span>
<span data-ttu-id="3f2ec-126">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3f2ec-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f2ec-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f2ec-127">-DefaultProfile</span></span>
<span data-ttu-id="3f2ec-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f2ec-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3f2ec-129">-DisplayName</span></span>
<span data-ttu-id="3f2ec-130">Anger visnings namnet på den användare eller grupp som du vill bevilja behörigheter för.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-130">Specifies the display name of the user or group for whom to grant permissions.</span></span>
<span data-ttu-id="3f2ec-131">Visnings namnet måste finnas i den Active Directory som är kopplad till det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-131">This display name must exist in the active directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="3f2ec-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f2ec-132">-InputObject</span></span>
<span data-ttu-id="3f2ec-133">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f2ec-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3f2ec-134">-ObjectId</span></span>
<span data-ttu-id="3f2ec-135">Anger objekt-ID: t för den användare eller grupp i Azure Active Directory som du vill bevilja behörigheter för.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-135">Specifies the object ID of the user or group in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f2ec-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f2ec-136">-ResourceGroupName</span></span>
<span data-ttu-id="3f2ec-137">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-137">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f2ec-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f2ec-138">-ResourceId</span></span>
<span data-ttu-id="3f2ec-139">Resurs-ID för Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-139">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f2ec-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3f2ec-140">-WorkspaceName</span></span>
<span data-ttu-id="3f2ec-141">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-141">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f2ec-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3f2ec-142">-Confirm</span></span>
<span data-ttu-id="3f2ec-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f2ec-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f2ec-144">-WhatIf</span></span>
<span data-ttu-id="3f2ec-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f2ec-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f2ec-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f2ec-147">CommonParameters</span></span>
<span data-ttu-id="3f2ec-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f2ec-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f2ec-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f2ec-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f2ec-150">INPUTS</span></span>

### <span data-ttu-id="3f2ec-151">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3f2ec-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3f2ec-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f2ec-152">OUTPUTS</span></span>

### <span data-ttu-id="3f2ec-153">Microsoft. Azure. commands. Synapse. Models. PSWorkspaceAadAdminInfo</span><span class="sxs-lookup"><span data-stu-id="3f2ec-153">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span></span>

## <span data-ttu-id="3f2ec-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f2ec-154">NOTES</span></span>

## <span data-ttu-id="3f2ec-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f2ec-155">RELATED LINKS</span></span>
