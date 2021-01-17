---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: d3ea1a67d8afa15549c19d6099dc727aab43adc5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424467"
---
# <span data-ttu-id="d97ec-101">Get-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="d97ec-101">Get-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="d97ec-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d97ec-102">SYNOPSIS</span></span>
<span data-ttu-id="d97ec-103">Hämtar information om en Azure AD-administratör för Synapse Analytics-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="d97ec-103">Gets information about an Azure AD administrator for Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="d97ec-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d97ec-104">SYNTAX</span></span>

### <span data-ttu-id="d97ec-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d97ec-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d97ec-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d97ec-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d97ec-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d97ec-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d97ec-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d97ec-108">DESCRIPTION</span></span>
<span data-ttu-id="d97ec-109">Cmdleten **Get-AzSynapseSqlActiveDirectoryAdministrator** hämtar information om en Azure Active Directory (Azure AD-administratör) för en Azure Synapse Analytics-arbetsyta i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="d97ec-109">The **Get-AzSynapseSqlActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an Azure Synapse Analytics Workspace in the current subscription.</span></span>

## <span data-ttu-id="d97ec-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d97ec-110">EXAMPLES</span></span>

### <span data-ttu-id="d97ec-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d97ec-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="d97ec-112">Det här kommandot får information om en Azure AD-administratör för en arbets yta med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="d97ec-112">This command gets information about an Azure AD administrator for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="d97ec-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d97ec-113">PARAMETERS</span></span>

### <span data-ttu-id="d97ec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d97ec-114">-DefaultProfile</span></span>
<span data-ttu-id="d97ec-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d97ec-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d97ec-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d97ec-116">-InputObject</span></span>
<span data-ttu-id="d97ec-117">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="d97ec-117">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d97ec-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d97ec-118">-ResourceGroupName</span></span>
<span data-ttu-id="d97ec-119">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="d97ec-119">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d97ec-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d97ec-120">-ResourceId</span></span>
<span data-ttu-id="d97ec-121">Resurs-ID för Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="d97ec-121">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d97ec-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d97ec-122">-WorkspaceName</span></span>
<span data-ttu-id="d97ec-123">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="d97ec-123">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d97ec-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d97ec-124">CommonParameters</span></span>
<span data-ttu-id="d97ec-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d97ec-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d97ec-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d97ec-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d97ec-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d97ec-127">INPUTS</span></span>

### <span data-ttu-id="d97ec-128">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d97ec-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d97ec-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d97ec-129">OUTPUTS</span></span>

### <span data-ttu-id="d97ec-130">Microsoft. Azure. commands. Synapse. Models. PSWorkspaceAadAdminInfo</span><span class="sxs-lookup"><span data-stu-id="d97ec-130">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span></span>

## <span data-ttu-id="d97ec-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d97ec-131">NOTES</span></span>

## <span data-ttu-id="d97ec-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d97ec-132">RELATED LINKS</span></span>
