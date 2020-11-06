---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: ae003c3c523c17db9c486edaa68d7e0991b0e6d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580635"
---
# <span data-ttu-id="f4707-101">Get-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="f4707-101">Get-AzureRmDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="f4707-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f4707-102">SYNOPSIS</span></span>
<span data-ttu-id="f4707-103">Hämtar den tillåtna principen för virtuell dator storlek för en laboratorie i DevTest-labb.</span><span class="sxs-lookup"><span data-stu-id="f4707-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4707-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f4707-104">SYNTAX</span></span>

```
Get-AzureRmDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4707-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f4707-105">DESCRIPTION</span></span>
<span data-ttu-id="f4707-106">Cmdleten **Get-AzureRmDtlAllowedVMSizesPolicy** hämtar den tillåtna storleken på den virtuella datorn, vilket gör att du kan ange en lista med storlekar för virtuell dator som är tillåtna i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="f4707-106">The **Get-AzureRmDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="f4707-107">Cmdleten returnerar den aktiverade eller inaktiverade statusen för principen och en lista över alla tillåtna storlekar på virtuella datorer som du har angett i den angivna principen.</span><span class="sxs-lookup"><span data-stu-id="f4707-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="f4707-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f4707-108">EXAMPLES</span></span>

## <span data-ttu-id="f4707-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f4707-109">PARAMETERS</span></span>

### <span data-ttu-id="f4707-110">-LabName</span><span class="sxs-lookup"><span data-stu-id="f4707-110">-LabName</span></span>
<span data-ttu-id="f4707-111">Anger namnet på den Lab för vilken denna cmdlet får storleks principen för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="f4707-111">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

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

### <span data-ttu-id="f4707-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4707-112">-ResourceGroupName</span></span>
<span data-ttu-id="f4707-113">Anger namnet på den resurs grupp som laboratoriet hör till.</span><span class="sxs-lookup"><span data-stu-id="f4707-113">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="f4707-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4707-114">-DefaultProfile</span></span>
<span data-ttu-id="f4707-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f4707-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4707-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4707-116">CommonParameters</span></span>
<span data-ttu-id="f4707-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4707-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4707-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4707-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4707-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f4707-119">INPUTS</span></span>

## <span data-ttu-id="f4707-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f4707-120">OUTPUTS</span></span>

### <span data-ttu-id="f4707-121">Microsoft. Azure. commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="f4707-121">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="f4707-122">Denna cmdlet returnerar den princip som anger listan med storlekar som är tillåtna i Lab.</span><span class="sxs-lookup"><span data-stu-id="f4707-122">This cmdlet returns the policy that specifies the list of virtual machine sizes allowed in the lab.</span></span>

## <span data-ttu-id="f4707-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f4707-123">NOTES</span></span>

## <span data-ttu-id="f4707-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f4707-124">RELATED LINKS</span></span>

[<span data-ttu-id="f4707-125">Set-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="f4707-125">Set-AzureRmDtlAllowedVMSizesPolicy</span></span>](./Set-AzureRmDtlAllowedVMSizesPolicy.md)

[<span data-ttu-id="f4707-126">Cmdlets för Azure Development Test Lab</span><span class="sxs-lookup"><span data-stu-id="f4707-126">Azure Development Test Lab Cmdlets</span></span>](./AzureRM.DevTestLabs.md)


