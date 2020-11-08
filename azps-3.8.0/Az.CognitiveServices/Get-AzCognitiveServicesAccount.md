---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccount.md
ms.openlocfilehash: 3f442cc975c6fdbb95d53153c2c80615bb8676a4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088045"
---
# <span data-ttu-id="3f2a8-101">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3f2a8-101">Get-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="3f2a8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f2a8-102">SYNOPSIS</span></span>
<span data-ttu-id="3f2a8-103">Hämtar ett konto.</span><span class="sxs-lookup"><span data-stu-id="3f2a8-103">Gets an account.</span></span>

## <span data-ttu-id="3f2a8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f2a8-104">SYNTAX</span></span>

### <span data-ttu-id="3f2a8-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f2a8-105">ResourceGroupParameterSet</span></span>
```
Get-AzCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f2a8-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f2a8-106">AccountNameParameterSet</span></span>
```
Get-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f2a8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f2a8-107">DESCRIPTION</span></span>
<span data-ttu-id="3f2a8-108">Cmdleten **Get-AzCognitiveServicesAccount** hämtar de etablerade kontona för kognitiva tjänster i resurs gruppen som anges av parametern *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="3f2a8-108">The **Get-AzCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="3f2a8-109">Om du inte anger parametern *ResourceGroupName* hämtar denna cmdlet alla kognitiva tjänst konton för den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="3f2a8-109">If you do not specify the *ResourceGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="3f2a8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f2a8-110">EXAMPLES</span></span>

### <span data-ttu-id="3f2a8-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3f2a8-111">Example 1</span></span>
```powershell
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locati
on 'WestUS'

ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WESTUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="3f2a8-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f2a8-112">PARAMETERS</span></span>

### <span data-ttu-id="3f2a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f2a8-113">-DefaultProfile</span></span>
<span data-ttu-id="3f2a8-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3f2a8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f2a8-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="3f2a8-115">-Name</span></span>
<span data-ttu-id="3f2a8-116">Anger namnet på det konto som du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="3f2a8-116">Specifies the name of the Cognitive Services account to get.</span></span>

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

### <span data-ttu-id="3f2a8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f2a8-117">-ResourceGroupName</span></span>
<span data-ttu-id="3f2a8-118">Anger namnet på resurs gruppen som är kopplat till det här kontot.</span><span class="sxs-lookup"><span data-stu-id="3f2a8-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="3f2a8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f2a8-119">CommonParameters</span></span>
<span data-ttu-id="3f2a8-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f2a8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f2a8-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f2a8-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f2a8-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f2a8-122">INPUTS</span></span>

### <span data-ttu-id="3f2a8-123">System. String</span><span class="sxs-lookup"><span data-stu-id="3f2a8-123">System.String</span></span>

## <span data-ttu-id="3f2a8-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f2a8-124">OUTPUTS</span></span>

### <span data-ttu-id="3f2a8-125">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3f2a8-125">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="3f2a8-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f2a8-126">NOTES</span></span>

## <span data-ttu-id="3f2a8-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f2a8-127">RELATED LINKS</span></span>

[<span data-ttu-id="3f2a8-128">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3f2a8-128">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="3f2a8-129">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3f2a8-129">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="3f2a8-130">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3f2a8-130">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)


