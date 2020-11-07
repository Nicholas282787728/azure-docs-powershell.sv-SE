---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: d76797f82a14c8efa2f9a3d6a77436fa2f8a1b68
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745382"
---
# <span data-ttu-id="54d4a-101">Get-AzEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="54d4a-101">Get-AzEnrollmentAccount</span></span>

## <span data-ttu-id="54d4a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54d4a-102">SYNOPSIS</span></span>
<span data-ttu-id="54d4a-103">Skaffa registrerings konton.</span><span class="sxs-lookup"><span data-stu-id="54d4a-103">Get enrollment accounts.</span></span>

## <span data-ttu-id="54d4a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54d4a-104">SYNTAX</span></span>

### <span data-ttu-id="54d4a-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="54d4a-105">List (Default)</span></span>
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54d4a-106">Enda</span><span class="sxs-lookup"><span data-stu-id="54d4a-106">Single</span></span>
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54d4a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54d4a-107">DESCRIPTION</span></span>
<span data-ttu-id="54d4a-108">Cmdleten **Get-AzEnrollmentAccount** hämtar registrerings konton.</span><span class="sxs-lookup"><span data-stu-id="54d4a-108">The **Get-AzEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="54d4a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54d4a-109">EXAMPLES</span></span>

### <span data-ttu-id="54d4a-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="54d4a-110">Example 1</span></span>
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="54d4a-111">Skaffa alla tillgängliga registrerings konton.</span><span class="sxs-lookup"><span data-stu-id="54d4a-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="54d4a-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="54d4a-112">Example 2</span></span>
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="54d4a-113">Skaffa registrerings kontot med angivet objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="54d4a-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="54d4a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54d4a-114">PARAMETERS</span></span>

### <span data-ttu-id="54d4a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54d4a-115">-DefaultProfile</span></span>
<span data-ttu-id="54d4a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="54d4a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54d4a-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="54d4a-117">-ObjectId</span></span>
<span data-ttu-id="54d4a-118">ObjectId för ett specifikt registrerings konto att få.</span><span class="sxs-lookup"><span data-stu-id="54d4a-118">ObjectId of a specific enrollment account to get.</span></span>

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

### <span data-ttu-id="54d4a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54d4a-119">CommonParameters</span></span>
<span data-ttu-id="54d4a-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54d4a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54d4a-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54d4a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54d4a-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54d4a-122">INPUTS</span></span>

### <span data-ttu-id="54d4a-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="54d4a-123">None</span></span>

## <span data-ttu-id="54d4a-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54d4a-124">OUTPUTS</span></span>

### <span data-ttu-id="54d4a-125">Microsoft. Azure. commands. Billing. Models. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="54d4a-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="54d4a-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54d4a-126">NOTES</span></span>

## <span data-ttu-id="54d4a-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54d4a-127">RELATED LINKS</span></span>
