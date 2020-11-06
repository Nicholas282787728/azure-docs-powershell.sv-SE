---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
ms.openlocfilehash: 247b0735e41f02a55b94e5a8f8ed44136eb3f37e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574538"
---
# <span data-ttu-id="aaad7-101">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="aaad7-101">Get-AzureRmADSpCredential</span></span>

## <span data-ttu-id="aaad7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aaad7-102">SYNOPSIS</span></span>
<span data-ttu-id="aaad7-103">Hämtar en lista med autentiseringsuppgifter som är associerade med ett tjänst huvud.</span><span class="sxs-lookup"><span data-stu-id="aaad7-103">Retrieves a list of credentials associated with a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aaad7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aaad7-104">SYNTAX</span></span>

### <span data-ttu-id="aaad7-105">ObjectIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="aaad7-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aaad7-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="aaad7-106">SPNParameterSet</span></span>
```
Get-AzureRmADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aaad7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aaad7-107">DESCRIPTION</span></span>
<span data-ttu-id="aaad7-108">Get-AzureRmADSpCredential cmdlet kan användas för att hämta en lista med autentiseringsuppgifter som är associerade med ett tjänst huvud.</span><span class="sxs-lookup"><span data-stu-id="aaad7-108">The Get-AzureRmADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="aaad7-109">Med det här kommandot hämtas alla egenskaper för autentiseringsuppgifter (men inte det Credential-värde) som är kopplat till tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="aaad7-109">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="aaad7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aaad7-110">EXAMPLES</span></span>

### <span data-ttu-id="aaad7-111">--------------------------Exempel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="aaad7-111">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Get-AzureRmADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="aaad7-112">Returnerar en lista med autentiseringsuppgifter som är kopplade till tjänstens huvud namn (SPN) http://test12345 .</span><span class="sxs-lookup"><span data-stu-id="aaad7-112">Returns a list of credentials associated with the service principal having SPN 'http://test12345'.</span></span>

## <span data-ttu-id="aaad7-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aaad7-113">PARAMETERS</span></span>

### <span data-ttu-id="aaad7-114">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="aaad7-114">-ObjectId</span></span>
<span data-ttu-id="aaad7-115">Objekt-ID för tjänstens huvud namn att hämta autentiseringsuppgifter från.</span><span class="sxs-lookup"><span data-stu-id="aaad7-115">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaad7-116">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="aaad7-116">-ServicePrincipalName</span></span>
<span data-ttu-id="aaad7-117">Namnet (SPN) för tjänstens huvud namn att hämta autentiseringsuppgifter från.</span><span class="sxs-lookup"><span data-stu-id="aaad7-117">The name (SPN) of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaad7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaad7-118">-DefaultProfile</span></span>
<span data-ttu-id="aaad7-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="aaad7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aaad7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaad7-120">CommonParameters</span></span>
<span data-ttu-id="aaad7-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaad7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaad7-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaad7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaad7-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aaad7-123">INPUTS</span></span>

## <span data-ttu-id="aaad7-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aaad7-124">OUTPUTS</span></span>

### <span data-ttu-id="aaad7-125">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="aaad7-125">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="aaad7-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aaad7-126">NOTES</span></span>

## <span data-ttu-id="aaad7-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aaad7-127">RELATED LINKS</span></span>

[<span data-ttu-id="aaad7-128">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="aaad7-128">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="aaad7-129">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="aaad7-129">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="aaad7-130">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="aaad7-130">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

