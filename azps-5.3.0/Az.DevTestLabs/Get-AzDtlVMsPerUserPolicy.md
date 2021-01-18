---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: f2d8604de126dcdfa830bdd6650cf66a6db391b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523700"
---
# <span data-ttu-id="15d38-101">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="15d38-101">Get-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="15d38-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="15d38-102">SYNOPSIS</span></span>
<span data-ttu-id="15d38-103">Hämtar en policy för virtuella datorer per användare i ett labb i DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="15d38-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="15d38-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="15d38-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15d38-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="15d38-105">DESCRIPTION</span></span>
<span data-ttu-id="15d38-106">Cmdleten **Get-AzDtlVMsPerUserPolicy** hämtar de virtuella datorerna per användar princip för ett labb, vilket gör att du kan ange maximalt antal virtuella datorer per användare.</span><span class="sxs-lookup"><span data-stu-id="15d38-106">The **Get-AzDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="15d38-107">Cmdleten returnerar den aktiverade eller inaktiverade statusen för principen och det högsta antalet virtuella datorer som du har angett i principen.</span><span class="sxs-lookup"><span data-stu-id="15d38-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="15d38-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="15d38-108">EXAMPLES</span></span>

## <span data-ttu-id="15d38-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="15d38-109">PARAMETERS</span></span>

### <span data-ttu-id="15d38-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15d38-110">-DefaultProfile</span></span>
<span data-ttu-id="15d38-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="15d38-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15d38-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="15d38-112">-LabName</span></span>
<span data-ttu-id="15d38-113">Anger namnet på den Lab för vilken denna cmdlet får principen för virtuell dator per användare.</span><span class="sxs-lookup"><span data-stu-id="15d38-113">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="15d38-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15d38-114">-ResourceGroupName</span></span>
<span data-ttu-id="15d38-115">Anger namnet på den resurs grupp som laboratoriet hör till.</span><span class="sxs-lookup"><span data-stu-id="15d38-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="15d38-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15d38-116">CommonParameters</span></span>
<span data-ttu-id="15d38-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15d38-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15d38-118">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15d38-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15d38-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="15d38-119">INPUTS</span></span>

### <span data-ttu-id="15d38-120">System. String</span><span class="sxs-lookup"><span data-stu-id="15d38-120">System.String</span></span>

## <span data-ttu-id="15d38-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="15d38-121">OUTPUTS</span></span>

### <span data-ttu-id="15d38-122">Microsoft. Azure. commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="15d38-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="15d38-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="15d38-123">NOTES</span></span>

## <span data-ttu-id="15d38-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="15d38-124">RELATED LINKS</span></span>

[<span data-ttu-id="15d38-125">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="15d38-125">Set-AzDtlVMsPerUserPolicy</span></span>](./Set-AzDtlVMsPerUserPolicy.md)


