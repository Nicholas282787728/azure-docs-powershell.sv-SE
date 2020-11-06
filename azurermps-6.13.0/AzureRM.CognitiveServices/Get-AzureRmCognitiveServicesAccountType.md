---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountType.md
ms.openlocfilehash: 05a4af3e92febcf30d44de9b114972a7c1f61d5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581752"
---
# <span data-ttu-id="12f6d-101">Get-AzureRmCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="12f6d-101">Get-AzureRmCognitiveServicesAccountType</span></span>

## <span data-ttu-id="12f6d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="12f6d-102">SYNOPSIS</span></span>
<span data-ttu-id="12f6d-103">Hämtar de tillgängliga konto typerna för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="12f6d-103">Gets the available Cognitive Services Account Types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12f6d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="12f6d-104">SYNTAX</span></span>

### <span data-ttu-id="12f6d-105">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="12f6d-105">GetAccountTypeWithName</span></span>
```
Get-AzureRmCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12f6d-106">GetAccountTypes</span><span class="sxs-lookup"><span data-stu-id="12f6d-106">GetAccountTypes</span></span>
```
Get-AzureRmCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="12f6d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="12f6d-107">DESCRIPTION</span></span>
<span data-ttu-id="12f6d-108">Cmdleten **Get-AzureRmCognitiveServicesAccountType** hämtar de tillgängliga konto typerna för kognitiva tjänster under det här abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="12f6d-108">The **Get-AzureRmCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="12f6d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="12f6d-109">EXAMPLES</span></span>

### <span data-ttu-id="12f6d-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="12f6d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType
```

<span data-ttu-id="12f6d-111">Hämta listan med tillgängliga typer.</span><span class="sxs-lookup"><span data-stu-id="12f6d-111">Get the list of available Types.</span></span>

### <span data-ttu-id="12f6d-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="12f6d-112">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="12f6d-113">Hämta listan med tillgängliga typer i väst.</span><span class="sxs-lookup"><span data-stu-id="12f6d-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="12f6d-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="12f6d-114">Example 3</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="12f6d-115">Kontrol lera om `Face` det är ett giltigt typnamn, att namnet returneras om det är ett giltigt namn.</span><span class="sxs-lookup"><span data-stu-id="12f6d-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="12f6d-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="12f6d-116">PARAMETERS</span></span>

### <span data-ttu-id="12f6d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12f6d-117">-DefaultProfile</span></span>
<span data-ttu-id="12f6d-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="12f6d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12f6d-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="12f6d-119">-Location</span></span>
<span data-ttu-id="12f6d-120">Konto plats för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="12f6d-120">Cognitive Services Account Location.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAccountTypes
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12f6d-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="12f6d-121">-TypeName</span></span>
<span data-ttu-id="12f6d-122">Konto typs namn för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="12f6d-122">Cognitive Services Account Type Name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAccountTypeWithName
Aliases: CognitiveServicesAccountTypeName, AccountTypeName, KindName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12f6d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12f6d-123">CommonParameters</span></span>
<span data-ttu-id="12f6d-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12f6d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12f6d-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12f6d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12f6d-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="12f6d-126">INPUTS</span></span>

### <span data-ttu-id="12f6d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="12f6d-127">System.String</span></span>

## <span data-ttu-id="12f6d-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="12f6d-128">OUTPUTS</span></span>

### <span data-ttu-id="12f6d-129">System. string []</span><span class="sxs-lookup"><span data-stu-id="12f6d-129">System.String[]</span></span>

### <span data-ttu-id="12f6d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="12f6d-130">System.String</span></span>

## <span data-ttu-id="12f6d-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="12f6d-131">NOTES</span></span>

## <span data-ttu-id="12f6d-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="12f6d-132">RELATED LINKS</span></span>
