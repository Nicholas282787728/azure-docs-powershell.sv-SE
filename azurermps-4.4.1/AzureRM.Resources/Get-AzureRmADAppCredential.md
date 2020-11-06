---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
ms.openlocfilehash: e270a59e3799302eed49a0fd60180bb8d4589d92
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585348"
---
# <span data-ttu-id="3faf4-101">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="3faf4-101">Get-AzureRmADAppCredential</span></span>

## <span data-ttu-id="3faf4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3faf4-102">SYNOPSIS</span></span>
<span data-ttu-id="3faf4-103">Hämtar en lista med autentiseringsuppgifter som är associerade med ett program.</span><span class="sxs-lookup"><span data-stu-id="3faf4-103">Retrieves a list of credentials associated with an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3faf4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3faf4-104">SYNTAX</span></span>

### <span data-ttu-id="3faf4-105">ApplicationObjectIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3faf4-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3faf4-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3faf4-106">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3faf4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3faf4-107">DESCRIPTION</span></span>
<span data-ttu-id="3faf4-108">Med cmdleten Get-AzureRmADAppCredential kan du hämta en lista med autentiseringsuppgifter som är associerade med ett program.</span><span class="sxs-lookup"><span data-stu-id="3faf4-108">The Get-AzureRmADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>

<span data-ttu-id="3faf4-109">Det här kommandot hämtar alla autentiseringsuppgifter-egenskaper (men inte referensvärdet) som är associerade med programmet.</span><span class="sxs-lookup"><span data-stu-id="3faf4-109">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="3faf4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3faf4-110">EXAMPLES</span></span>

### <span data-ttu-id="3faf4-111">--------------------------Exempel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3faf4-111">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Get-AzureRmADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="3faf4-112">Returnerar en lista med autentiseringsuppgifter som är kopplade till programmet med objekt-ID ' 1f99cf81-0146-4f4e-BEAE-2007d0668476 '.</span><span class="sxs-lookup"><span data-stu-id="3faf4-112">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

## <span data-ttu-id="3faf4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3faf4-113">PARAMETERS</span></span>

### <span data-ttu-id="3faf4-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3faf4-114">-ApplicationId</span></span>
<span data-ttu-id="3faf4-115">ID för programmet som autentiseringsuppgifterna hämtas från.</span><span class="sxs-lookup"><span data-stu-id="3faf4-115">The id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3faf4-116">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3faf4-116">-ObjectId</span></span>
<span data-ttu-id="3faf4-117">Objekt-ID för programmet som du vill hämta autentiseringsuppgifter från.</span><span class="sxs-lookup"><span data-stu-id="3faf4-117">The object id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3faf4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3faf4-118">-DefaultProfile</span></span>
<span data-ttu-id="3faf4-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3faf4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3faf4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3faf4-120">CommonParameters</span></span>
<span data-ttu-id="3faf4-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3faf4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3faf4-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3faf4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3faf4-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3faf4-123">INPUTS</span></span>

## <span data-ttu-id="3faf4-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3faf4-124">OUTPUTS</span></span>

### <span data-ttu-id="3faf4-125">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="3faf4-125">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="3faf4-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3faf4-126">NOTES</span></span>

## <span data-ttu-id="3faf4-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3faf4-127">RELATED LINKS</span></span>

[<span data-ttu-id="3faf4-128">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="3faf4-128">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="3faf4-129">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="3faf4-129">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="3faf4-130">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="3faf4-130">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

