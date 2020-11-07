---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAks.md
ms.openlocfilehash: 34db847ba7a4051efab32a62c667d3d79ad4ac30
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743481"
---
# <span data-ttu-id="232de-101">Get-AzAks</span><span class="sxs-lookup"><span data-stu-id="232de-101">Get-AzAks</span></span>

## <span data-ttu-id="232de-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="232de-102">SYNOPSIS</span></span>
<span data-ttu-id="232de-103">Lista Kubernetes hanterade kluster.</span><span class="sxs-lookup"><span data-stu-id="232de-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="232de-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="232de-104">SYNTAX</span></span>

### <span data-ttu-id="232de-105">ResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="232de-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAks [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="232de-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="232de-106">IdParameterSet</span></span>
```
Get-AzAks [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="232de-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="232de-107">NameParameterSet</span></span>
```
Get-AzAks [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="232de-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="232de-108">DESCRIPTION</span></span>
<span data-ttu-id="232de-109">Lista Kubernetes hanterade kluster.</span><span class="sxs-lookup"><span data-stu-id="232de-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="232de-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="232de-110">EXAMPLES</span></span>

### <span data-ttu-id="232de-111">Lista alla Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="232de-111">List all Kubernetes clusters</span></span>
```
PS C:\> Get-AzAks
```

## <span data-ttu-id="232de-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="232de-112">PARAMETERS</span></span>

### <span data-ttu-id="232de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="232de-113">-DefaultProfile</span></span>
<span data-ttu-id="232de-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="232de-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="232de-115">-ID</span><span class="sxs-lookup"><span data-stu-id="232de-115">-Id</span></span>
<span data-ttu-id="232de-116">ID för ett hanterat Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="232de-116">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="232de-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="232de-117">-Name</span></span>
<span data-ttu-id="232de-118">Namn på ditt hanterade Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="232de-118">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="232de-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="232de-119">-ResourceGroupName</span></span>
<span data-ttu-id="232de-120">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="232de-120">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="232de-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="232de-121">CommonParameters</span></span>
<span data-ttu-id="232de-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="232de-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="232de-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="232de-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="232de-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="232de-124">INPUTS</span></span>

### <span data-ttu-id="232de-125">System. String</span><span class="sxs-lookup"><span data-stu-id="232de-125">System.String</span></span>

## <span data-ttu-id="232de-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="232de-126">OUTPUTS</span></span>

### <span data-ttu-id="232de-127">Microsoft. Azure. commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="232de-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="232de-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="232de-128">NOTES</span></span>

## <span data-ttu-id="232de-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="232de-129">RELATED LINKS</span></span>
