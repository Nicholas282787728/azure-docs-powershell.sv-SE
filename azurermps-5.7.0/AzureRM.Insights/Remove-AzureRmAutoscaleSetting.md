---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
ms.openlocfilehash: 4d6c2f748915847038ef4029dc024763375ef99e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575660"
---
# <span data-ttu-id="b89aa-101">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b89aa-101">Remove-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="b89aa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b89aa-102">SYNOPSIS</span></span>
<span data-ttu-id="b89aa-103">Tar bort en autoskalningsinställning.</span><span class="sxs-lookup"><span data-stu-id="b89aa-103">Removes an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b89aa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b89aa-104">SYNTAX</span></span>

```
Remove-AzureRmAutoscaleSetting -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b89aa-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b89aa-105">DESCRIPTION</span></span>
<span data-ttu-id="b89aa-106">Cmdleten **Remove-AzureRmAutoscaleSetting** tar bort en autoskalningsinställning.</span><span class="sxs-lookup"><span data-stu-id="b89aa-106">The **Remove-AzureRmAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="b89aa-107">Du måste ange namnet på inställningen och namnet på resurs gruppen som den har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="b89aa-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>

<span data-ttu-id="b89aa-108">Denna cmdlet implementerar ShouldProcess-mönstret, t. ex. det kan begära bekräftelse från användaren innan de skapar, ändrar eller tar bort resursen.</span><span class="sxs-lookup"><span data-stu-id="b89aa-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="b89aa-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b89aa-109">EXAMPLES</span></span>

## <span data-ttu-id="b89aa-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b89aa-110">PARAMETERS</span></span>

### <span data-ttu-id="b89aa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b89aa-111">-DefaultProfile</span></span>
<span data-ttu-id="b89aa-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b89aa-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b89aa-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="b89aa-113">-Name</span></span>
<span data-ttu-id="b89aa-114">Anger namnet på den autoskalningsinställning som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="b89aa-114">Specifies the name of the Autoscale setting to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b89aa-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b89aa-115">-ResourceGroupName</span></span>
<span data-ttu-id="b89aa-116">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b89aa-116">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b89aa-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b89aa-117">CommonParameters</span></span>
<span data-ttu-id="b89aa-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b89aa-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b89aa-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b89aa-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b89aa-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b89aa-120">INPUTS</span></span>

### <span data-ttu-id="b89aa-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="b89aa-121">None</span></span>
<span data-ttu-id="b89aa-122">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="b89aa-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b89aa-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b89aa-123">OUTPUTS</span></span>

### <span data-ttu-id="b89aa-124">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b89aa-124">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="b89aa-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b89aa-125">NOTES</span></span>

## <span data-ttu-id="b89aa-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b89aa-126">RELATED LINKS</span></span>

[<span data-ttu-id="b89aa-127">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b89aa-127">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="b89aa-128">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b89aa-128">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)


