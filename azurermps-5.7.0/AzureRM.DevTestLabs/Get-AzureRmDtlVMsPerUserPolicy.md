---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerUserPolicy.md
ms.openlocfilehash: 53afed94f9733c041df2c49ff1ec97a2fb8277f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575665"
---
# <span data-ttu-id="0da8d-101">Get-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="0da8d-101">Get-AzureRmDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="0da8d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0da8d-102">SYNOPSIS</span></span>
<span data-ttu-id="0da8d-103">Hämtar en policy för virtuella datorer per användare i ett labb i DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="0da8d-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0da8d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0da8d-104">SYNTAX</span></span>

```
Get-AzureRmDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0da8d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0da8d-105">DESCRIPTION</span></span>
<span data-ttu-id="0da8d-106">Cmdleten **Get-AzureRmDtlVMsPerUserPolicy** hämtar de virtuella datorerna per användar princip för ett labb, vilket gör att du kan ange maximalt antal virtuella datorer per användare.</span><span class="sxs-lookup"><span data-stu-id="0da8d-106">The **Get-AzureRmDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="0da8d-107">Cmdleten returnerar den aktiverade eller inaktiverade statusen för principen och det högsta antalet virtuella datorer som du har angett i principen.</span><span class="sxs-lookup"><span data-stu-id="0da8d-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="0da8d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0da8d-108">EXAMPLES</span></span>

## <span data-ttu-id="0da8d-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0da8d-109">PARAMETERS</span></span>

### <span data-ttu-id="0da8d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0da8d-110">-DefaultProfile</span></span>
<span data-ttu-id="0da8d-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0da8d-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0da8d-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="0da8d-112">-LabName</span></span>
<span data-ttu-id="0da8d-113">Anger namnet på den Lab för vilken denna cmdlet får principen för virtuell dator per användare.</span><span class="sxs-lookup"><span data-stu-id="0da8d-113">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="0da8d-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0da8d-114">-ResourceGroupName</span></span>
<span data-ttu-id="0da8d-115">Anger namnet på den resurs grupp som laboratoriet hör till.</span><span class="sxs-lookup"><span data-stu-id="0da8d-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0da8d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0da8d-116">CommonParameters</span></span>
<span data-ttu-id="0da8d-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0da8d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0da8d-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0da8d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0da8d-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0da8d-119">INPUTS</span></span>

### <span data-ttu-id="0da8d-120">Ingen</span><span class="sxs-lookup"><span data-stu-id="0da8d-120">None</span></span>
<span data-ttu-id="0da8d-121">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="0da8d-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0da8d-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0da8d-122">OUTPUTS</span></span>

### <span data-ttu-id="0da8d-123">Microsoft. Azure. commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="0da8d-123">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="0da8d-124">Denna cmdlet returnerar den princip som anger maximalt antal virtuella datorer som kan skapas av en användare i labbet.</span><span class="sxs-lookup"><span data-stu-id="0da8d-124">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created by a user in the lab.</span></span>

## <span data-ttu-id="0da8d-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0da8d-125">NOTES</span></span>

## <span data-ttu-id="0da8d-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0da8d-126">RELATED LINKS</span></span>

[<span data-ttu-id="0da8d-127">Set-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="0da8d-127">Set-AzureRmDtlVMsPerUserPolicy</span></span>](./Set-AzureRmDtlVMsPerUserPolicy.md)


