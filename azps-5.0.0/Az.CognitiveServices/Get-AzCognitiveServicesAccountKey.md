---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: 8150abc726f990b699237dbaad3641a99bae2e2c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271645"
---
# <span data-ttu-id="9ff11-101">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="9ff11-101">Get-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="9ff11-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9ff11-102">SYNOPSIS</span></span>
<span data-ttu-id="9ff11-103">Hämtar API-nycklarna för ett konto.</span><span class="sxs-lookup"><span data-stu-id="9ff11-103">Gets the API keys for an account.</span></span>

## <span data-ttu-id="9ff11-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9ff11-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ff11-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9ff11-105">DESCRIPTION</span></span>
<span data-ttu-id="9ff11-106">Cmdleten **Get-AzCognitiveServicesAccountKey** hämtar API-nycklarna för ett etablerat konto för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="9ff11-106">The **Get-AzCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>
<span data-ttu-id="9ff11-107">Ett konto för kognitiva tjänster har två API-nycklar: KEY1 och Key2.</span><span class="sxs-lookup"><span data-stu-id="9ff11-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="9ff11-108">Nycklarna aktiverar interaktion med konto slut punkten för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="9ff11-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>
<span data-ttu-id="9ff11-109">Använd New-AzCognitiveServicesAccountKey för att återskapa en nyckeln.</span><span class="sxs-lookup"><span data-stu-id="9ff11-109">Use New-AzCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="9ff11-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9ff11-110">EXAMPLES</span></span>

### <span data-ttu-id="9ff11-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9ff11-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="9ff11-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9ff11-112">PARAMETERS</span></span>

### <span data-ttu-id="9ff11-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ff11-113">-DefaultProfile</span></span>
<span data-ttu-id="9ff11-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9ff11-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ff11-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="9ff11-115">-Name</span></span>
<span data-ttu-id="9ff11-116">Anger namnet på kontot.</span><span class="sxs-lookup"><span data-stu-id="9ff11-116">Specifies the name of the account.</span></span>
<span data-ttu-id="9ff11-117">Denna cmdlet hämtar nycklarna för det här kontot.</span><span class="sxs-lookup"><span data-stu-id="9ff11-117">This cmdlet gets the keys for this account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ff11-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ff11-118">-ResourceGroupName</span></span>
<span data-ttu-id="9ff11-119">Anger namnet på resurs gruppen som kontot är tilldelat till.</span><span class="sxs-lookup"><span data-stu-id="9ff11-119">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="9ff11-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ff11-120">CommonParameters</span></span>
<span data-ttu-id="9ff11-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ff11-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ff11-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ff11-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ff11-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9ff11-123">INPUTS</span></span>

### <span data-ttu-id="9ff11-124">System. String</span><span class="sxs-lookup"><span data-stu-id="9ff11-124">System.String</span></span>

## <span data-ttu-id="9ff11-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9ff11-125">OUTPUTS</span></span>

### <span data-ttu-id="9ff11-126">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSCognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9ff11-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="9ff11-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9ff11-127">NOTES</span></span>

## <span data-ttu-id="9ff11-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9ff11-128">RELATED LINKS</span></span>

[<span data-ttu-id="9ff11-129">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="9ff11-129">New-AzCognitiveServicesAccountKey</span></span>](./New-AzCognitiveServicesAccountKey.md)


