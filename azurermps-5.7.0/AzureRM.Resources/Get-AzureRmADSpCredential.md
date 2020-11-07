---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
ms.openlocfilehash: 8c03dd19fd2995347a3b4ae52de04fdcb3f02c30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756074"
---
# <span data-ttu-id="67e82-101">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="67e82-101">Get-AzureRmADSpCredential</span></span>

## <span data-ttu-id="67e82-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="67e82-102">SYNOPSIS</span></span>
<span data-ttu-id="67e82-103">Hämtar en lista med autentiseringsuppgifter som är associerade med ett tjänst huvud.</span><span class="sxs-lookup"><span data-stu-id="67e82-103">Retrieves a list of credentials associated with a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67e82-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="67e82-104">SYNTAX</span></span>

### <span data-ttu-id="67e82-105">ObjectIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="67e82-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67e82-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="67e82-106">SPNParameterSet</span></span>
```
Get-AzureRmADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67e82-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="67e82-107">DESCRIPTION</span></span>
<span data-ttu-id="67e82-108">Get-AzureRmADSpCredential cmdlet kan användas för att hämta en lista med autentiseringsuppgifter som är associerade med ett tjänst huvud.</span><span class="sxs-lookup"><span data-stu-id="67e82-108">The Get-AzureRmADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="67e82-109">Med det här kommandot hämtas alla egenskaper för autentiseringsuppgifter (men inte det Credential-värde) som är kopplat till tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="67e82-109">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="67e82-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="67e82-110">EXAMPLES</span></span>

### <span data-ttu-id="67e82-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="67e82-111">Example 1</span></span>
```
PS E:\> Get-AzureRmADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="67e82-112">Returnerar en lista med autentiseringsuppgifter som är kopplade till tjänstens huvud namn (SPN) http://test12345 .</span><span class="sxs-lookup"><span data-stu-id="67e82-112">Returns a list of credentials associated with the service principal having SPN 'http://test12345'.</span></span>

## <span data-ttu-id="67e82-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="67e82-113">PARAMETERS</span></span>

### <span data-ttu-id="67e82-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67e82-114">-DefaultProfile</span></span>
<span data-ttu-id="67e82-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="67e82-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67e82-116">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="67e82-116">-ObjectId</span></span>
<span data-ttu-id="67e82-117">Objekt-ID för tjänstens huvud namn att hämta autentiseringsuppgifter från.</span><span class="sxs-lookup"><span data-stu-id="67e82-117">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67e82-118">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="67e82-118">-ServicePrincipalName</span></span>
<span data-ttu-id="67e82-119">Namnet (SPN) för tjänstens huvud namn att hämta autentiseringsuppgifter från.</span><span class="sxs-lookup"><span data-stu-id="67e82-119">The name (SPN) of the service principal to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: SPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67e82-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67e82-120">CommonParameters</span></span>
<span data-ttu-id="67e82-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67e82-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67e82-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67e82-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67e82-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="67e82-123">INPUTS</span></span>

### <span data-ttu-id="67e82-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="67e82-124">None</span></span>
<span data-ttu-id="67e82-125">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="67e82-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="67e82-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="67e82-126">OUTPUTS</span></span>

### <span data-ttu-id="67e82-127">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="67e82-127">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="67e82-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="67e82-128">NOTES</span></span>

## <span data-ttu-id="67e82-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="67e82-129">RELATED LINKS</span></span>

[<span data-ttu-id="67e82-130">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="67e82-130">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="67e82-131">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="67e82-131">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="67e82-132">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="67e82-132">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

