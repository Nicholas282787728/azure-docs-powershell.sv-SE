---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/get-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Get-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Get-AzureRmAks.md
ms.openlocfilehash: d30d9858a3050864f5cc86601adf6b598be8c54d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581851"
---
# <span data-ttu-id="afba0-101">Get-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="afba0-101">Get-AzureRmAks</span></span>

## <span data-ttu-id="afba0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="afba0-102">SYNOPSIS</span></span>
<span data-ttu-id="afba0-103">Lista Kubernetes hanterade kluster.</span><span class="sxs-lookup"><span data-stu-id="afba0-103">List Kubernetes managed clusters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afba0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="afba0-104">SYNTAX</span></span>

### <span data-ttu-id="afba0-105">ResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="afba0-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmAks [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afba0-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="afba0-106">IdParameterSet</span></span>
```
Get-AzureRmAks [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afba0-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="afba0-107">NameParameterSet</span></span>
```
Get-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="afba0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="afba0-108">DESCRIPTION</span></span>
<span data-ttu-id="afba0-109">Lista Kubernetes hanterade kluster.</span><span class="sxs-lookup"><span data-stu-id="afba0-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="afba0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="afba0-110">EXAMPLES</span></span>

### <span data-ttu-id="afba0-111">Lista alla Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="afba0-111">List all Kubernetes clusters</span></span>
```
PS C:\> Get-AzureRmAks
```

## <span data-ttu-id="afba0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="afba0-112">PARAMETERS</span></span>

### <span data-ttu-id="afba0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afba0-113">-DefaultProfile</span></span>
<span data-ttu-id="afba0-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="afba0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afba0-115">-ID</span><span class="sxs-lookup"><span data-stu-id="afba0-115">-Id</span></span>
<span data-ttu-id="afba0-116">ID för ett hanterat Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="afba0-116">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="afba0-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="afba0-117">-Name</span></span>
<span data-ttu-id="afba0-118">Namn på ditt hanterade Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="afba0-118">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="afba0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afba0-119">-ResourceGroupName</span></span>
<span data-ttu-id="afba0-120">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="afba0-120">Resource group name</span></span>

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

### <span data-ttu-id="afba0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afba0-121">CommonParameters</span></span>
<span data-ttu-id="afba0-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afba0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afba0-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afba0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afba0-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="afba0-124">INPUTS</span></span>

### <span data-ttu-id="afba0-125">System. String</span><span class="sxs-lookup"><span data-stu-id="afba0-125">System.String</span></span>

## <span data-ttu-id="afba0-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="afba0-126">OUTPUTS</span></span>

### <span data-ttu-id="afba0-127">Microsoft. Azure. commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="afba0-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="afba0-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="afba0-128">NOTES</span></span>

## <span data-ttu-id="afba0-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="afba0-129">RELATED LINKS</span></span>
