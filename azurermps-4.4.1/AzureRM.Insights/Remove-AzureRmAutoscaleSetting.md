---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
ms.openlocfilehash: cd853184e06403f3c0d516ee1b0790c724adacb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582419"
---
# <span data-ttu-id="f8db9-101">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="f8db9-101">Remove-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="f8db9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f8db9-102">SYNOPSIS</span></span>
<span data-ttu-id="f8db9-103">Tar bort en autoskalningsinställning.</span><span class="sxs-lookup"><span data-stu-id="f8db9-103">Removes an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8db9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f8db9-104">SYNTAX</span></span>

```
Remove-AzureRmAutoscaleSetting -ResourceGroup <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8db9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f8db9-105">DESCRIPTION</span></span>
<span data-ttu-id="f8db9-106">Cmdleten **Remove-AzureRmAutoscaleSetting** tar bort en autoskalningsinställning.</span><span class="sxs-lookup"><span data-stu-id="f8db9-106">The **Remove-AzureRmAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="f8db9-107">Du måste ange namnet på inställningen och namnet på resurs gruppen som den har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="f8db9-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>

## <span data-ttu-id="f8db9-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f8db9-108">EXAMPLES</span></span>

## <span data-ttu-id="f8db9-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f8db9-109">PARAMETERS</span></span>

### <span data-ttu-id="f8db9-110">-Namn</span><span class="sxs-lookup"><span data-stu-id="f8db9-110">-Name</span></span>
<span data-ttu-id="f8db9-111">Anger namnet på den autoskalningsinställning som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="f8db9-111">Specifies the name of the Autoscale setting to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8db9-112">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f8db9-112">-ResourceGroup</span></span>
<span data-ttu-id="f8db9-113">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f8db9-113">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8db9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8db9-114">-DefaultProfile</span></span>
<span data-ttu-id="f8db9-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f8db9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8db9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8db9-116">CommonParameters</span></span>
<span data-ttu-id="f8db9-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8db9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8db9-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8db9-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8db9-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f8db9-119">INPUTS</span></span>

## <span data-ttu-id="f8db9-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f8db9-120">OUTPUTS</span></span>

### <span data-ttu-id="f8db9-121">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f8db9-121">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="f8db9-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f8db9-122">NOTES</span></span>

## <span data-ttu-id="f8db9-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f8db9-123">RELATED LINKS</span></span>

[<span data-ttu-id="f8db9-124">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="f8db9-124">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="f8db9-125">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="f8db9-125">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)


