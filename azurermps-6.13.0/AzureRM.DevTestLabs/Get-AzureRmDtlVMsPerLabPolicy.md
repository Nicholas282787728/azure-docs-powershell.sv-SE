---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: A3F653C7-6F9D-4B2B-81F8-0A012D80ECC7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerLabPolicy.md
ms.openlocfilehash: 3f38c8ace41a1f125a37053f136cd61c597787ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576294"
---
# <span data-ttu-id="b9047-101">Get-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="b9047-101">Get-AzureRmDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="b9047-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b9047-102">SYNOPSIS</span></span>
<span data-ttu-id="b9047-103">Hämtar de virtuella datorerna per labb policy för ett labb i DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="b9047-103">Gets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9047-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b9047-104">SYNTAX</span></span>

```
Get-AzureRmDtlVMsPerLabPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9047-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b9047-105">DESCRIPTION</span></span>
<span data-ttu-id="b9047-106">Cmdleten **Get-AzureRmDtlVMsPerLabPolicy** hämtar de virtuella datorerna per Lab-princip för ett labb, vilket gör att du kan ange totalt antal virtuella datorer som är tillåtna i ett labb.</span><span class="sxs-lookup"><span data-stu-id="b9047-106">The **Get-AzureRmDtlVMsPerLabPolicy** cmdlet gets the virtual machines per lab policy of a lab, which allows you set the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="b9047-107">Cmdleten returnerar den aktiverade eller inaktiverade statusen för principen och totalt antal virtuella datorer som är tillåtna i den laboratorium som du har angett i principen.</span><span class="sxs-lookup"><span data-stu-id="b9047-107">The cmdlet returns the enabled or disabled status of the policy, and the total number of virtual machines allowed in the lab that you have set in the policy.</span></span>

## <span data-ttu-id="b9047-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b9047-108">EXAMPLES</span></span>

## <span data-ttu-id="b9047-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b9047-109">PARAMETERS</span></span>

### <span data-ttu-id="b9047-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9047-110">-DefaultProfile</span></span>
<span data-ttu-id="b9047-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b9047-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9047-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="b9047-112">-LabName</span></span>
<span data-ttu-id="b9047-113">Anger namnet på den Lab för vilken denna cmdlet får de virtuella datorerna.</span><span class="sxs-lookup"><span data-stu-id="b9047-113">Specifies the name of the lab for which this cmdlet gets the virtual machines.</span></span>

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

### <span data-ttu-id="b9047-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9047-114">-ResourceGroupName</span></span>
<span data-ttu-id="b9047-115">Anger namnet på den resurs grupp som laboratoriet hör till.</span><span class="sxs-lookup"><span data-stu-id="b9047-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="b9047-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9047-116">CommonParameters</span></span>
<span data-ttu-id="b9047-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9047-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9047-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9047-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9047-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b9047-119">INPUTS</span></span>

### <span data-ttu-id="b9047-120">System. String</span><span class="sxs-lookup"><span data-stu-id="b9047-120">System.String</span></span>

## <span data-ttu-id="b9047-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b9047-121">OUTPUTS</span></span>

### <span data-ttu-id="b9047-122">Microsoft. Azure. commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="b9047-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="b9047-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b9047-123">NOTES</span></span>

## <span data-ttu-id="b9047-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b9047-124">RELATED LINKS</span></span>

[<span data-ttu-id="b9047-125">Set-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="b9047-125">Set-AzureRmDtlVMsPerLabPolicy</span></span>](./Set-AzureRmDtlVMsPerLabPolicy.md)

