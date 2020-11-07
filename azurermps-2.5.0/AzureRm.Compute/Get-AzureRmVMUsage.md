---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmusage
schema: 2.0.0
ms.openlocfilehash: 210c66f91836b40c719d91907fc78bd907d0fe86
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931510"
---
# <span data-ttu-id="024fa-101">Get-AzureRmVMUsage</span><span class="sxs-lookup"><span data-stu-id="024fa-101">Get-AzureRmVMUsage</span></span>

## <span data-ttu-id="024fa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="024fa-102">SYNOPSIS</span></span>
<span data-ttu-id="024fa-103">Hämtar användning för antal virtuella datorer för en plats.</span><span class="sxs-lookup"><span data-stu-id="024fa-103">Gets the virtual machine core count usage for a location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="024fa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="024fa-104">SYNTAX</span></span>

```
Get-AzureRmVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="024fa-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="024fa-105">DESCRIPTION</span></span>
<span data-ttu-id="024fa-106">Cmdleten **Get-AzureRmVMUsage** hämtar användnings utrymmet för virtuella datorer för en plats.</span><span class="sxs-lookup"><span data-stu-id="024fa-106">The **Get-AzureRmVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="024fa-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="024fa-107">EXAMPLES</span></span>

### <span data-ttu-id="024fa-108">Exempel 1: Hämta användning av antal kärnor för en plats</span><span class="sxs-lookup"><span data-stu-id="024fa-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

<span data-ttu-id="024fa-109">Det här kommandot får användning av kärn beräkning av virtuella datorer för plats centralen.</span><span class="sxs-lookup"><span data-stu-id="024fa-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="024fa-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="024fa-110">PARAMETERS</span></span>

### <span data-ttu-id="024fa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="024fa-111">-DefaultProfile</span></span>
<span data-ttu-id="024fa-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="024fa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="024fa-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="024fa-113">-Location</span></span>
<span data-ttu-id="024fa-114">Anger den plats där den här cmdleten får användning av kärn antal virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="024fa-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="024fa-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="024fa-115">CommonParameters</span></span>
<span data-ttu-id="024fa-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="024fa-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="024fa-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="024fa-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="024fa-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="024fa-118">INPUTS</span></span>

### <span data-ttu-id="024fa-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="024fa-119">None</span></span>
<span data-ttu-id="024fa-120">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="024fa-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="024fa-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="024fa-121">OUTPUTS</span></span>

### <span data-ttu-id="024fa-122">Microsoft. Azure. commands. Compute. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="024fa-122">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="024fa-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="024fa-123">NOTES</span></span>

## <span data-ttu-id="024fa-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="024fa-124">RELATED LINKS</span></span>

[<span data-ttu-id="024fa-125">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="024fa-125">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


