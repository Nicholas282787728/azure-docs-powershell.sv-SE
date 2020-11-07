---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
ms.openlocfilehash: d5d43a0aebcc553a230655d52399081548aae209
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757139"
---
# <span data-ttu-id="928f8-101">Get-AzureRmEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="928f8-101">Get-AzureRmEnrollmentAccount</span></span>

## <span data-ttu-id="928f8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="928f8-102">SYNOPSIS</span></span>
<span data-ttu-id="928f8-103">Skaffa registrerings konton.</span><span class="sxs-lookup"><span data-stu-id="928f8-103">Get enrollment accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="928f8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="928f8-104">SYNTAX</span></span>

### <span data-ttu-id="928f8-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="928f8-105">List (Default)</span></span>
```
Get-AzureRmEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="928f8-106">Enda</span><span class="sxs-lookup"><span data-stu-id="928f8-106">Single</span></span>
```
Get-AzureRmEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="928f8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="928f8-107">DESCRIPTION</span></span>
<span data-ttu-id="928f8-108">Cmdleten **Get-AzureRmEnrollmentAccount** hämtar registrerings konton.</span><span class="sxs-lookup"><span data-stu-id="928f8-108">The **Get-AzureRmEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="928f8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="928f8-109">EXAMPLES</span></span>

### <span data-ttu-id="928f8-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="928f8-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="928f8-111">Skaffa alla tillgängliga registrerings konton.</span><span class="sxs-lookup"><span data-stu-id="928f8-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="928f8-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="928f8-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="928f8-113">Skaffa registrerings kontot med angivet objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="928f8-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="928f8-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="928f8-114">PARAMETERS</span></span>

### <span data-ttu-id="928f8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="928f8-115">-DefaultProfile</span></span>
<span data-ttu-id="928f8-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="928f8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="928f8-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="928f8-117">-ObjectId</span></span>
<span data-ttu-id="928f8-118">ObjectId för ett specifikt registrerings konto att få.</span><span class="sxs-lookup"><span data-stu-id="928f8-118">ObjectId of a specific enrollment account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Single
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="928f8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="928f8-119">CommonParameters</span></span>
<span data-ttu-id="928f8-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="928f8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="928f8-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="928f8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="928f8-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="928f8-122">INPUTS</span></span>

### <span data-ttu-id="928f8-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="928f8-123">None</span></span>

## <span data-ttu-id="928f8-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="928f8-124">OUTPUTS</span></span>

### <span data-ttu-id="928f8-125">Microsoft. Azure. commands. Billing. Models. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="928f8-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="928f8-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="928f8-126">NOTES</span></span>

## <span data-ttu-id="928f8-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="928f8-127">RELATED LINKS</span></span>
