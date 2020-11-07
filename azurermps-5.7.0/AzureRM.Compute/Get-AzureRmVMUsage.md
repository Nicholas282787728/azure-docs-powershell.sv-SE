---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
ms.openlocfilehash: 5d4f114ef93e0febf7c113f73b8007a9322be752
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757705"
---
# <span data-ttu-id="f0039-101">Get-AzureRmVMUsage</span><span class="sxs-lookup"><span data-stu-id="f0039-101">Get-AzureRmVMUsage</span></span>

## <span data-ttu-id="f0039-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f0039-102">SYNOPSIS</span></span>
<span data-ttu-id="f0039-103">Hämtar användning för antal virtuella datorer för en plats.</span><span class="sxs-lookup"><span data-stu-id="f0039-103">Gets the virtual machine core count usage for a location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0039-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f0039-104">SYNTAX</span></span>

```
Get-AzureRmVMUsage [-Location] <String> [<CommonParameters>]
```

## <span data-ttu-id="f0039-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f0039-105">DESCRIPTION</span></span>
<span data-ttu-id="f0039-106">Cmdleten **Get-AzureRmVMUsage** hämtar användnings utrymmet för virtuella datorer för en plats.</span><span class="sxs-lookup"><span data-stu-id="f0039-106">The **Get-AzureRmVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="f0039-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f0039-107">EXAMPLES</span></span>

### <span data-ttu-id="f0039-108">Exempel 1: Hämta användning av antal kärnor för en plats</span><span class="sxs-lookup"><span data-stu-id="f0039-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

<span data-ttu-id="f0039-109">Det här kommandot får användning av kärn beräkning av virtuella datorer för plats centralen.</span><span class="sxs-lookup"><span data-stu-id="f0039-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="f0039-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f0039-110">PARAMETERS</span></span>

### <span data-ttu-id="f0039-111">-Plats</span><span class="sxs-lookup"><span data-stu-id="f0039-111">-Location</span></span>
<span data-ttu-id="f0039-112">Anger den plats där den här cmdleten får användning av kärn antal virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="f0039-112">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0039-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0039-113">CommonParameters</span></span>
<span data-ttu-id="f0039-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0039-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0039-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0039-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0039-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f0039-116">INPUTS</span></span>

### <span data-ttu-id="f0039-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="f0039-117">None</span></span>
<span data-ttu-id="f0039-118">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="f0039-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f0039-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f0039-119">OUTPUTS</span></span>

## <span data-ttu-id="f0039-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f0039-120">NOTES</span></span>

## <span data-ttu-id="f0039-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f0039-121">RELATED LINKS</span></span>

[<span data-ttu-id="f0039-122">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f0039-122">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


