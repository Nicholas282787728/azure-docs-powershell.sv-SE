---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMUsage.md
ms.openlocfilehash: 22f77bfc5802527103dd0e391a11e16833696abd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580284"
---
# <span data-ttu-id="8ecd8-101">Get-AzureRmVMUsage</span><span class="sxs-lookup"><span data-stu-id="8ecd8-101">Get-AzureRmVMUsage</span></span>

## <span data-ttu-id="8ecd8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8ecd8-102">SYNOPSIS</span></span>
<span data-ttu-id="8ecd8-103">Hämtar användning för antal virtuella datorer för en plats.</span><span class="sxs-lookup"><span data-stu-id="8ecd8-103">Gets the virtual machine core count usage for a location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ecd8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8ecd8-104">SYNTAX</span></span>

```
Get-AzureRmVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ecd8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8ecd8-105">DESCRIPTION</span></span>
<span data-ttu-id="8ecd8-106">Cmdleten **Get-AzureRmVMUsage** hämtar användnings utrymmet för virtuella datorer för en plats.</span><span class="sxs-lookup"><span data-stu-id="8ecd8-106">The **Get-AzureRmVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="8ecd8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8ecd8-107">EXAMPLES</span></span>

### <span data-ttu-id="8ecd8-108">Exempel 1: Hämta användning av antal kärnor för en plats</span><span class="sxs-lookup"><span data-stu-id="8ecd8-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

<span data-ttu-id="8ecd8-109">Det här kommandot får användning av kärn beräkning av virtuella datorer för plats centralen.</span><span class="sxs-lookup"><span data-stu-id="8ecd8-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="8ecd8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8ecd8-110">PARAMETERS</span></span>

### <span data-ttu-id="8ecd8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ecd8-111">-DefaultProfile</span></span>
<span data-ttu-id="8ecd8-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8ecd8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ecd8-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="8ecd8-113">-Location</span></span>
<span data-ttu-id="8ecd8-114">Anger den plats där den här cmdleten får användning av kärn antal virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="8ecd8-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ecd8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ecd8-115">CommonParameters</span></span>
<span data-ttu-id="8ecd8-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ecd8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ecd8-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ecd8-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ecd8-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8ecd8-118">INPUTS</span></span>

### <span data-ttu-id="8ecd8-119">System. String</span><span class="sxs-lookup"><span data-stu-id="8ecd8-119">System.String</span></span>

## <span data-ttu-id="8ecd8-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8ecd8-120">OUTPUTS</span></span>

### <span data-ttu-id="8ecd8-121">Microsoft. Azure. commands. Compute. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="8ecd8-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="8ecd8-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8ecd8-122">NOTES</span></span>

## <span data-ttu-id="8ecd8-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8ecd8-123">RELATED LINKS</span></span>

[<span data-ttu-id="8ecd8-124">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8ecd8-124">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


