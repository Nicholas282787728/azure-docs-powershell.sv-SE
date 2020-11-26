---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 8e4fbc28d52e8431122b8593b68b909554df6dc9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263285"
---
# <span data-ttu-id="2dc4b-101">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="2dc4b-101">Get-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="2dc4b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2dc4b-102">SYNOPSIS</span></span>
<span data-ttu-id="2dc4b-103">Hämtar den tillåtna principen för virtuell dator storlek för en laboratorie i DevTest-labb.</span><span class="sxs-lookup"><span data-stu-id="2dc4b-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="2dc4b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2dc4b-104">SYNTAX</span></span>

```
Get-AzDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2dc4b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2dc4b-105">DESCRIPTION</span></span>
<span data-ttu-id="2dc4b-106">Cmdleten **Get-AzDtlAllowedVMSizesPolicy** hämtar den tillåtna storleken på den virtuella datorn, vilket gör att du kan ange en lista med storlekar för virtuell dator som är tillåtna i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="2dc4b-106">The **Get-AzDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="2dc4b-107">Cmdleten returnerar den aktiverade eller inaktiverade statusen för principen och en lista över alla tillåtna storlekar på virtuella datorer som du har angett i den angivna principen.</span><span class="sxs-lookup"><span data-stu-id="2dc4b-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="2dc4b-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2dc4b-108">EXAMPLES</span></span>

## <span data-ttu-id="2dc4b-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2dc4b-109">PARAMETERS</span></span>

### <span data-ttu-id="2dc4b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dc4b-110">-DefaultProfile</span></span>
<span data-ttu-id="2dc4b-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2dc4b-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2dc4b-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="2dc4b-112">-LabName</span></span>
<span data-ttu-id="2dc4b-113">Anger namnet på den Lab för vilken denna cmdlet får storleks principen för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="2dc4b-113">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

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

### <span data-ttu-id="2dc4b-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dc4b-114">-ResourceGroupName</span></span>
<span data-ttu-id="2dc4b-115">Anger namnet på den resurs grupp som laboratoriet hör till.</span><span class="sxs-lookup"><span data-stu-id="2dc4b-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dc4b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dc4b-116">CommonParameters</span></span>
<span data-ttu-id="2dc4b-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dc4b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dc4b-118">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dc4b-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dc4b-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2dc4b-119">INPUTS</span></span>

### <span data-ttu-id="2dc4b-120">System. String</span><span class="sxs-lookup"><span data-stu-id="2dc4b-120">System.String</span></span>

## <span data-ttu-id="2dc4b-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2dc4b-121">OUTPUTS</span></span>

### <span data-ttu-id="2dc4b-122">Microsoft. Azure. commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="2dc4b-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="2dc4b-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2dc4b-123">NOTES</span></span>

## <span data-ttu-id="2dc4b-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2dc4b-124">RELATED LINKS</span></span>

[<span data-ttu-id="2dc4b-125">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="2dc4b-125">Set-AzDtlAllowedVMSizesPolicy</span></span>](./Set-AzDtlAllowedVMSizesPolicy.md)

