---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
ms.openlocfilehash: fa2368e1982e66d8edecc465d1f6ded3a3d75205
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576428"
---
# <span data-ttu-id="b59d8-101">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="b59d8-101">Get-AzureRmADAppCredential</span></span>

## <span data-ttu-id="b59d8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b59d8-102">SYNOPSIS</span></span>
<span data-ttu-id="b59d8-103">Hämtar en lista med autentiseringsuppgifter som är associerade med ett program.</span><span class="sxs-lookup"><span data-stu-id="b59d8-103">Retrieves a list of credentials associated with an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b59d8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b59d8-104">SYNTAX</span></span>

### <span data-ttu-id="b59d8-105">ApplicationObjectIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b59d8-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b59d8-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b59d8-106">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b59d8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b59d8-107">DESCRIPTION</span></span>
<span data-ttu-id="b59d8-108">Med cmdleten Get-AzureRmADAppCredential kan du hämta en lista med autentiseringsuppgifter som är associerade med ett program.</span><span class="sxs-lookup"><span data-stu-id="b59d8-108">The Get-AzureRmADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>

<span data-ttu-id="b59d8-109">Det här kommandot hämtar alla autentiseringsuppgifter-egenskaper (men inte referensvärdet) som är associerade med programmet.</span><span class="sxs-lookup"><span data-stu-id="b59d8-109">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="b59d8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b59d8-110">EXAMPLES</span></span>

### <span data-ttu-id="b59d8-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b59d8-111">Example 1</span></span>
```
PS E:\> Get-AzureRmADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="b59d8-112">Returnerar en lista med autentiseringsuppgifter som är kopplade till programmet med objekt-ID ' 1f99cf81-0146-4f4e-BEAE-2007d0668476 '.</span><span class="sxs-lookup"><span data-stu-id="b59d8-112">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

## <span data-ttu-id="b59d8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b59d8-113">PARAMETERS</span></span>

### <span data-ttu-id="b59d8-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b59d8-114">-ApplicationId</span></span>
<span data-ttu-id="b59d8-115">ID för programmet som autentiseringsuppgifterna hämtas från.</span><span class="sxs-lookup"><span data-stu-id="b59d8-115">The id of the application to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b59d8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b59d8-116">-DefaultProfile</span></span>
<span data-ttu-id="b59d8-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b59d8-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b59d8-118">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b59d8-118">-ObjectId</span></span>
<span data-ttu-id="b59d8-119">Objekt-ID för programmet som du vill hämta autentiseringsuppgifter från.</span><span class="sxs-lookup"><span data-stu-id="b59d8-119">The object id of the application to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b59d8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b59d8-120">CommonParameters</span></span>
<span data-ttu-id="b59d8-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b59d8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b59d8-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b59d8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b59d8-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b59d8-123">INPUTS</span></span>

### <span data-ttu-id="b59d8-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="b59d8-124">None</span></span>
<span data-ttu-id="b59d8-125">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="b59d8-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b59d8-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b59d8-126">OUTPUTS</span></span>

### <span data-ttu-id="b59d8-127">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="b59d8-127">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="b59d8-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b59d8-128">NOTES</span></span>

## <span data-ttu-id="b59d8-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b59d8-129">RELATED LINKS</span></span>

[<span data-ttu-id="b59d8-130">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="b59d8-130">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="b59d8-131">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="b59d8-131">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="b59d8-132">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="b59d8-132">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

