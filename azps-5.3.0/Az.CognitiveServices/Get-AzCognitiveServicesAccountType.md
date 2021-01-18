---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
ms.openlocfilehash: a99ca4bb636ba1767fc5f50611d3c5a9eb991312
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524589"
---
# <span data-ttu-id="17090-101">Get-AzCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="17090-101">Get-AzCognitiveServicesAccountType</span></span>

## <span data-ttu-id="17090-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="17090-102">SYNOPSIS</span></span>
<span data-ttu-id="17090-103">Hämtar de tillgängliga konto typerna för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="17090-103">Gets the available Cognitive Services Account Types.</span></span>

## <span data-ttu-id="17090-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="17090-104">SYNTAX</span></span>

### <span data-ttu-id="17090-105">GetAccountTypes (standard)</span><span class="sxs-lookup"><span data-stu-id="17090-105">GetAccountTypes (Default)</span></span>
```
Get-AzCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="17090-106">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="17090-106">GetAccountTypeWithName</span></span>
```
Get-AzCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="17090-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="17090-107">DESCRIPTION</span></span>
<span data-ttu-id="17090-108">Cmdleten **Get-AzCognitiveServicesAccountType** hämtar de tillgängliga konto typerna för kognitiva tjänster under det här abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="17090-108">The **Get-AzCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="17090-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="17090-109">EXAMPLES</span></span>

### <span data-ttu-id="17090-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="17090-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType
```

<span data-ttu-id="17090-111">Hämta listan med tillgängliga typer.</span><span class="sxs-lookup"><span data-stu-id="17090-111">Get the list of available Types.</span></span>

### <span data-ttu-id="17090-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="17090-112">Example 2</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="17090-113">Hämta listan med tillgängliga typer i väst.</span><span class="sxs-lookup"><span data-stu-id="17090-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="17090-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="17090-114">Example 3</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="17090-115">Kontrol lera om `Face` det är ett giltigt typnamn, att namnet returneras om det är ett giltigt namn.</span><span class="sxs-lookup"><span data-stu-id="17090-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="17090-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="17090-116">PARAMETERS</span></span>

### <span data-ttu-id="17090-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17090-117">-DefaultProfile</span></span>
<span data-ttu-id="17090-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="17090-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17090-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="17090-119">-Location</span></span>
<span data-ttu-id="17090-120">Konto plats för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="17090-120">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="17090-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="17090-121">-TypeName</span></span>
<span data-ttu-id="17090-122">Konto typs namn för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="17090-122">Cognitive Services Account Type Name.</span></span>

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

### <span data-ttu-id="17090-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17090-123">CommonParameters</span></span>
<span data-ttu-id="17090-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17090-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17090-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17090-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17090-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="17090-126">INPUTS</span></span>

### <span data-ttu-id="17090-127">System. String</span><span class="sxs-lookup"><span data-stu-id="17090-127">System.String</span></span>

## <span data-ttu-id="17090-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="17090-128">OUTPUTS</span></span>

### <span data-ttu-id="17090-129">System. string []</span><span class="sxs-lookup"><span data-stu-id="17090-129">System.String[]</span></span>

### <span data-ttu-id="17090-130">System. String</span><span class="sxs-lookup"><span data-stu-id="17090-130">System.String</span></span>

## <span data-ttu-id="17090-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="17090-131">NOTES</span></span>

## <span data-ttu-id="17090-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="17090-132">RELATED LINKS</span></span>
