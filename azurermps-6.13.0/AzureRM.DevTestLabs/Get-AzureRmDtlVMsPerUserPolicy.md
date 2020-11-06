---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerUserPolicy.md
ms.openlocfilehash: 4d8bf2922d58190e41e71e17c96ab55b5ee9433f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576292"
---
# <span data-ttu-id="d0de7-101">Get-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="d0de7-101">Get-AzureRmDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="d0de7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d0de7-102">SYNOPSIS</span></span>
<span data-ttu-id="d0de7-103">Hämtar en policy för virtuella datorer per användare i ett labb i DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="d0de7-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0de7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d0de7-104">SYNTAX</span></span>

```
Get-AzureRmDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0de7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d0de7-105">DESCRIPTION</span></span>
<span data-ttu-id="d0de7-106">Cmdleten **Get-AzureRmDtlVMsPerUserPolicy** hämtar de virtuella datorerna per användar princip för ett labb, vilket gör att du kan ange maximalt antal virtuella datorer per användare.</span><span class="sxs-lookup"><span data-stu-id="d0de7-106">The **Get-AzureRmDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="d0de7-107">Cmdleten returnerar den aktiverade eller inaktiverade statusen för principen och det högsta antalet virtuella datorer som du har angett i principen.</span><span class="sxs-lookup"><span data-stu-id="d0de7-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="d0de7-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d0de7-108">EXAMPLES</span></span>

## <span data-ttu-id="d0de7-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d0de7-109">PARAMETERS</span></span>

### <span data-ttu-id="d0de7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0de7-110">-DefaultProfile</span></span>
<span data-ttu-id="d0de7-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d0de7-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0de7-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="d0de7-112">-LabName</span></span>
<span data-ttu-id="d0de7-113">Anger namnet på den Lab för vilken denna cmdlet får principen för virtuell dator per användare.</span><span class="sxs-lookup"><span data-stu-id="d0de7-113">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="d0de7-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0de7-114">-ResourceGroupName</span></span>
<span data-ttu-id="d0de7-115">Anger namnet på den resurs grupp som laboratoriet hör till.</span><span class="sxs-lookup"><span data-stu-id="d0de7-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="d0de7-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0de7-116">CommonParameters</span></span>
<span data-ttu-id="d0de7-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0de7-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0de7-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0de7-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0de7-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d0de7-119">INPUTS</span></span>

### <span data-ttu-id="d0de7-120">System. String</span><span class="sxs-lookup"><span data-stu-id="d0de7-120">System.String</span></span>

## <span data-ttu-id="d0de7-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d0de7-121">OUTPUTS</span></span>

### <span data-ttu-id="d0de7-122">Microsoft. Azure. commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="d0de7-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="d0de7-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d0de7-123">NOTES</span></span>

## <span data-ttu-id="d0de7-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d0de7-124">RELATED LINKS</span></span>

[<span data-ttu-id="d0de7-125">Set-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="d0de7-125">Set-AzureRmDtlVMsPerUserPolicy</span></span>](./Set-AzureRmDtlVMsPerUserPolicy.md)


