---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmContainerService.md
ms.openlocfilehash: d2a53d221adf7483899056791aefd00b03aca26e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578320"
---
# <span data-ttu-id="5fbaa-101">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="5fbaa-101">Get-AzureRmContainerService</span></span>

## <span data-ttu-id="5fbaa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5fbaa-102">SYNOPSIS</span></span>
<span data-ttu-id="5fbaa-103">Hämtar en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-103">Gets a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fbaa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5fbaa-104">SYNTAX</span></span>

```
Get-AzureRmContainerService [[-ResourceGroupName] <String>] [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="5fbaa-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5fbaa-105">DESCRIPTION</span></span>
<span data-ttu-id="5fbaa-106">Cmdleten **Get-AzureRmContainerService** hämtar en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-106">The **Get-AzureRmContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="5fbaa-107">Du kan visa egenskaperna för en behållar tjänst, vilket inkluderar tillstånd, antalet huvud och agenter samt det fullt kvalificerade domän namnet för huvud gruppen och agenten.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="5fbaa-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5fbaa-108">EXAMPLES</span></span>

### <span data-ttu-id="5fbaa-109">Exempel 1: skaffa en behållar tjänst</span><span class="sxs-lookup"><span data-stu-id="5fbaa-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="5fbaa-110">Det här kommandot får en behållar tjänst som heter CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="5fbaa-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5fbaa-111">PARAMETERS</span></span>

### <span data-ttu-id="5fbaa-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="5fbaa-112">-Name</span></span>
<span data-ttu-id="5fbaa-113">Anger namnet på den behållar tjänst som cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-113">Specifies the name of the container service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fbaa-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fbaa-114">-ResourceGroupName</span></span>
<span data-ttu-id="5fbaa-115">Anger resurs gruppen för den behållar tjänst som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-115">Specifies the resource group of the container service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fbaa-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fbaa-116">CommonParameters</span></span>
<span data-ttu-id="5fbaa-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fbaa-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fbaa-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fbaa-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5fbaa-119">INPUTS</span></span>

### <span data-ttu-id="5fbaa-120">Ingen</span><span class="sxs-lookup"><span data-stu-id="5fbaa-120">None</span></span>
<span data-ttu-id="5fbaa-121">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5fbaa-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5fbaa-122">OUTPUTS</span></span>

## <span data-ttu-id="5fbaa-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5fbaa-123">NOTES</span></span>

## <span data-ttu-id="5fbaa-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5fbaa-124">RELATED LINKS</span></span>

[<span data-ttu-id="5fbaa-125">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="5fbaa-125">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="5fbaa-126">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="5fbaa-126">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="5fbaa-127">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="5fbaa-127">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


