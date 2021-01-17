---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
ms.openlocfilehash: e7d84439b2292d70604f3f7d9e827a0d8cc035e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392003"
---
# <span data-ttu-id="424c7-101">Get-AzContainerRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="424c7-101">Get-AzContainerRegistryUsage</span></span>

## <span data-ttu-id="424c7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="424c7-102">SYNOPSIS</span></span>
<span data-ttu-id="424c7-103">Få användning av en Azure-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="424c7-103">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="424c7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="424c7-104">SYNTAX</span></span>

```
Get-AzContainerRegistryUsage -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="424c7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="424c7-105">DESCRIPTION</span></span>
<span data-ttu-id="424c7-106">Få användning av en Azure-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="424c7-106">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="424c7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="424c7-107">EXAMPLES</span></span>

### <span data-ttu-id="424c7-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="424c7-108">Example 1</span></span>
```powershell
PS C:\> Get-AzContainerRegistryUsage -ResourceGroupName $resourceGroupName -RegistryName $RegistryName
```

<span data-ttu-id="424c7-109">Få användning av en Azure-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="424c7-109">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="424c7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="424c7-110">PARAMETERS</span></span>

### <span data-ttu-id="424c7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="424c7-111">-DefaultProfile</span></span>
<span data-ttu-id="424c7-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="424c7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="424c7-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="424c7-113">-Name</span></span>
<span data-ttu-id="424c7-114">Mål register namn.</span><span class="sxs-lookup"><span data-stu-id="424c7-114">Target registry name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RegistryName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="424c7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="424c7-115">-ResourceGroupName</span></span>
<span data-ttu-id="424c7-116">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="424c7-116">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="424c7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="424c7-117">CommonParameters</span></span>
<span data-ttu-id="424c7-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="424c7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="424c7-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="424c7-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="424c7-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="424c7-120">INPUTS</span></span>

### <span data-ttu-id="424c7-121">System. String</span><span class="sxs-lookup"><span data-stu-id="424c7-121">System.String</span></span>

## <span data-ttu-id="424c7-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="424c7-122">OUTPUTS</span></span>

### <span data-ttu-id="424c7-123">Microsoft. Azure. commands. ContainerRegistry. Models. PSRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="424c7-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span></span>

## <span data-ttu-id="424c7-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="424c7-124">NOTES</span></span>

## <span data-ttu-id="424c7-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="424c7-125">RELATED LINKS</span></span>
