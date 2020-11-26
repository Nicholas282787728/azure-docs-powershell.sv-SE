---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
ms.openlocfilehash: d2702c28a4cedc0198f3fb767f0e509912269a63
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261140"
---
# <span data-ttu-id="e9858-101">Get-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="e9858-101">Get-AzAksCluster</span></span>

## <span data-ttu-id="e9858-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e9858-102">SYNOPSIS</span></span>
<span data-ttu-id="e9858-103">Lista Kubernetes hanterade kluster.</span><span class="sxs-lookup"><span data-stu-id="e9858-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="e9858-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e9858-104">SYNTAX</span></span>

### <span data-ttu-id="e9858-105">ResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e9858-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAksCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9858-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9858-106">IdParameterSet</span></span>
```
Get-AzAksCluster [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9858-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9858-107">NameParameterSet</span></span>
```
Get-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9858-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e9858-108">DESCRIPTION</span></span>
<span data-ttu-id="e9858-109">Lista Kubernetes hanterade kluster.</span><span class="sxs-lookup"><span data-stu-id="e9858-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="e9858-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e9858-110">EXAMPLES</span></span>

### <span data-ttu-id="e9858-111">Lista alla Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="e9858-111">List all Kubernetes clusters</span></span>
```powershell
PS C:\> Get-AzAksCluster
```

## <span data-ttu-id="e9858-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e9858-112">PARAMETERS</span></span>

### <span data-ttu-id="e9858-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9858-113">-DefaultProfile</span></span>
<span data-ttu-id="e9858-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e9858-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9858-115">-ID</span><span class="sxs-lookup"><span data-stu-id="e9858-115">-Id</span></span>
<span data-ttu-id="e9858-116">ID för ett hanterat Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="e9858-116">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="e9858-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="e9858-117">-Name</span></span>
<span data-ttu-id="e9858-118">Namn på ditt hanterade Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="e9858-118">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="e9858-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9858-119">-ResourceGroupName</span></span>
<span data-ttu-id="e9858-120">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="e9858-120">Resource group name</span></span>

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

### <span data-ttu-id="e9858-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9858-121">CommonParameters</span></span>
<span data-ttu-id="e9858-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9858-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9858-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9858-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9858-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e9858-124">INPUTS</span></span>

### <span data-ttu-id="e9858-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e9858-125">System.String</span></span>

## <span data-ttu-id="e9858-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e9858-126">OUTPUTS</span></span>

### <span data-ttu-id="e9858-127">Microsoft. Azure. commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="e9858-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="e9858-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e9858-128">NOTES</span></span>

## <span data-ttu-id="e9858-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e9858-129">RELATED LINKS</span></span>