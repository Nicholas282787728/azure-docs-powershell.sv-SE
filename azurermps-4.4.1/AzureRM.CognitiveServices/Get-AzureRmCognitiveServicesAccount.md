---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: c4419707c9c536a21e5fdc8aa39326b02e21937c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578415"
---
# <span data-ttu-id="6d1b9-101">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="6d1b9-101">Get-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="6d1b9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6d1b9-102">SYNOPSIS</span></span>
<span data-ttu-id="6d1b9-103">Hämtar ett konto.</span><span class="sxs-lookup"><span data-stu-id="6d1b9-103">Gets an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d1b9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6d1b9-104">SYNTAX</span></span>

### <span data-ttu-id="6d1b9-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d1b9-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6d1b9-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d1b9-106">AccountNameParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d1b9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6d1b9-107">DESCRIPTION</span></span>
<span data-ttu-id="6d1b9-108">Cmdleten **Get-AzureRmCognitiveServicesAccount** hämtar de etablerade kontona för kognitiva tjänster i resurs gruppen som anges av parametern *ResoureGroupName* .</span><span class="sxs-lookup"><span data-stu-id="6d1b9-108">The **Get-AzureRmCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResoureGroupName* parameter.</span></span>

<span data-ttu-id="6d1b9-109">Om du inte anger parametern *ResoureGroupName* hämtar denna cmdlet alla kognitiva tjänst konton för den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="6d1b9-109">If you do not specify the *ResoureGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="6d1b9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6d1b9-110">EXAMPLES</span></span>

## <span data-ttu-id="6d1b9-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6d1b9-111">PARAMETERS</span></span>

### <span data-ttu-id="6d1b9-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="6d1b9-112">-Name</span></span>
<span data-ttu-id="6d1b9-113">Anger namnet på det konto som du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="6d1b9-113">Specifies the name of the Cognitive Services account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d1b9-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d1b9-114">-ResourceGroupName</span></span>
<span data-ttu-id="6d1b9-115">Anger namnet på resurs gruppen som är kopplat till det här kontot.</span><span class="sxs-lookup"><span data-stu-id="6d1b9-115">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d1b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d1b9-116">-DefaultProfile</span></span>
<span data-ttu-id="6d1b9-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6d1b9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d1b9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d1b9-118">CommonParameters</span></span>
<span data-ttu-id="6d1b9-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d1b9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d1b9-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d1b9-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d1b9-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6d1b9-121">INPUTS</span></span>

## <span data-ttu-id="6d1b9-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6d1b9-122">OUTPUTS</span></span>

### <span data-ttu-id="6d1b9-123">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="6d1b9-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="6d1b9-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6d1b9-124">NOTES</span></span>

## <span data-ttu-id="6d1b9-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6d1b9-125">RELATED LINKS</span></span>

[<span data-ttu-id="6d1b9-126">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="6d1b9-126">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="6d1b9-127">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="6d1b9-127">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="6d1b9-128">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="6d1b9-128">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)


