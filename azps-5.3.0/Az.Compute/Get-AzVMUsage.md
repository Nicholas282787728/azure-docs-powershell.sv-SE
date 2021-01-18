---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: d22e36ad3cc4737be9c73d6b7cdc49329f904263
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524508"
---
# <span data-ttu-id="7f7b4-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="7f7b4-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="7f7b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7f7b4-102">SYNOPSIS</span></span>
<span data-ttu-id="7f7b4-103">Hämtar användning för antal virtuella datorer för en plats.</span><span class="sxs-lookup"><span data-stu-id="7f7b4-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="7f7b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7f7b4-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f7b4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7f7b4-105">DESCRIPTION</span></span>
<span data-ttu-id="7f7b4-106">Cmdleten **Get-AzVMUsage** hämtar användnings utrymmet för virtuella datorer för en plats.</span><span class="sxs-lookup"><span data-stu-id="7f7b4-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="7f7b4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7f7b4-107">EXAMPLES</span></span>

### <span data-ttu-id="7f7b4-108">Exempel 1: Hämta användning av antal kärnor för en plats</span><span class="sxs-lookup"><span data-stu-id="7f7b4-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="7f7b4-109">Det här kommandot får användning av kärn beräkning av virtuella datorer för plats centralen.</span><span class="sxs-lookup"><span data-stu-id="7f7b4-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="7f7b4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7f7b4-110">PARAMETERS</span></span>

### <span data-ttu-id="7f7b4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f7b4-111">-DefaultProfile</span></span>
<span data-ttu-id="7f7b4-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7f7b4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f7b4-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="7f7b4-113">-Location</span></span>
<span data-ttu-id="7f7b4-114">Anger den plats där den här cmdleten får användning av kärn antal virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="7f7b4-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="7f7b4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f7b4-115">CommonParameters</span></span>
<span data-ttu-id="7f7b4-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f7b4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f7b4-117">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f7b4-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f7b4-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7f7b4-118">INPUTS</span></span>

### <span data-ttu-id="7f7b4-119">System. String</span><span class="sxs-lookup"><span data-stu-id="7f7b4-119">System.String</span></span>

## <span data-ttu-id="7f7b4-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7f7b4-120">OUTPUTS</span></span>

### <span data-ttu-id="7f7b4-121">Microsoft. Azure. commands. Compute. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="7f7b4-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="7f7b4-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7f7b4-122">NOTES</span></span>

## <span data-ttu-id="7f7b4-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7f7b4-123">RELATED LINKS</span></span>

[<span data-ttu-id="7f7b4-124">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="7f7b4-124">Get-AzVM</span></span>](./Get-AzVM.md)


