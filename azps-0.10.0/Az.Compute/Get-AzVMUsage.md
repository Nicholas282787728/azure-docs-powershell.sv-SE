---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: 66a74ed2fa389c0dd39fa9fc86570ff8d68dc1dc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925134"
---
# <span data-ttu-id="6595b-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="6595b-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="6595b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6595b-102">SYNOPSIS</span></span>
<span data-ttu-id="6595b-103">Hämtar användning för antal virtuella datorer för en plats.</span><span class="sxs-lookup"><span data-stu-id="6595b-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="6595b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6595b-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6595b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6595b-105">DESCRIPTION</span></span>
<span data-ttu-id="6595b-106">Cmdleten **Get-AzVMUsage** hämtar användnings utrymmet för virtuella datorer för en plats.</span><span class="sxs-lookup"><span data-stu-id="6595b-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="6595b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6595b-107">EXAMPLES</span></span>

### <span data-ttu-id="6595b-108">Exempel 1: Hämta användning av antal kärnor för en plats</span><span class="sxs-lookup"><span data-stu-id="6595b-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="6595b-109">Det här kommandot får användning av kärn beräkning av virtuella datorer för plats centralen.</span><span class="sxs-lookup"><span data-stu-id="6595b-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="6595b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6595b-110">PARAMETERS</span></span>

### <span data-ttu-id="6595b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6595b-111">-DefaultProfile</span></span>
<span data-ttu-id="6595b-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6595b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6595b-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="6595b-113">-Location</span></span>
<span data-ttu-id="6595b-114">Anger den plats där den här cmdleten får användning av kärn antal virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="6595b-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="6595b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6595b-115">CommonParameters</span></span>
<span data-ttu-id="6595b-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6595b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6595b-117">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6595b-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6595b-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6595b-118">INPUTS</span></span>

### <span data-ttu-id="6595b-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="6595b-119">None</span></span>
<span data-ttu-id="6595b-120">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="6595b-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6595b-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6595b-121">OUTPUTS</span></span>

### <span data-ttu-id="6595b-122">Microsoft. Azure. commands. Compute. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="6595b-122">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="6595b-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6595b-123">NOTES</span></span>

## <span data-ttu-id="6595b-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6595b-124">RELATED LINKS</span></span>

[<span data-ttu-id="6595b-125">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="6595b-125">Get-AzVM</span></span>](./Get-AzVM.md)


