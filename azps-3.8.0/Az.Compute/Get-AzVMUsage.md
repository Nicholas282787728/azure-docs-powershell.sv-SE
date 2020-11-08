---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: d22e36ad3cc4737be9c73d6b7cdc49329f904263
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088208"
---
# <span data-ttu-id="0fb4a-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="0fb4a-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="0fb4a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0fb4a-102">SYNOPSIS</span></span>
<span data-ttu-id="0fb4a-103">Hämtar användning för antal virtuella datorer för en plats.</span><span class="sxs-lookup"><span data-stu-id="0fb4a-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="0fb4a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0fb4a-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fb4a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0fb4a-105">DESCRIPTION</span></span>
<span data-ttu-id="0fb4a-106">Cmdleten **Get-AzVMUsage** hämtar användnings utrymmet för virtuella datorer för en plats.</span><span class="sxs-lookup"><span data-stu-id="0fb4a-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="0fb4a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0fb4a-107">EXAMPLES</span></span>

### <span data-ttu-id="0fb4a-108">Exempel 1: Hämta användning av antal kärnor för en plats</span><span class="sxs-lookup"><span data-stu-id="0fb4a-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="0fb4a-109">Det här kommandot får användning av kärn beräkning av virtuella datorer för plats centralen.</span><span class="sxs-lookup"><span data-stu-id="0fb4a-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="0fb4a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0fb4a-110">PARAMETERS</span></span>

### <span data-ttu-id="0fb4a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fb4a-111">-DefaultProfile</span></span>
<span data-ttu-id="0fb4a-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0fb4a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fb4a-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="0fb4a-113">-Location</span></span>
<span data-ttu-id="0fb4a-114">Anger den plats där den här cmdleten får användning av kärn antal virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="0fb4a-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="0fb4a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fb4a-115">CommonParameters</span></span>
<span data-ttu-id="0fb4a-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fb4a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fb4a-117">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0fb4a-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fb4a-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0fb4a-118">INPUTS</span></span>

### <span data-ttu-id="0fb4a-119">System. String</span><span class="sxs-lookup"><span data-stu-id="0fb4a-119">System.String</span></span>

## <span data-ttu-id="0fb4a-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0fb4a-120">OUTPUTS</span></span>

### <span data-ttu-id="0fb4a-121">Microsoft. Azure. commands. Compute. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="0fb4a-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="0fb4a-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0fb4a-122">NOTES</span></span>

## <span data-ttu-id="0fb4a-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0fb4a-123">RELATED LINKS</span></span>

[<span data-ttu-id="0fb4a-124">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="0fb4a-124">Get-AzVM</span></span>](./Get-AzVM.md)


