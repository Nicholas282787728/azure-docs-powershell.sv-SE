---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
ms.openlocfilehash: d0efe107f15cf3e2bcb0d25c283fee306eeb404b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574402"
---
# <span data-ttu-id="16d35-101">Get-AzureRmEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="16d35-101">Get-AzureRmEnrollmentAccount</span></span>

## <span data-ttu-id="16d35-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="16d35-102">SYNOPSIS</span></span>
<span data-ttu-id="16d35-103">Skaffa registrerings konton.</span><span class="sxs-lookup"><span data-stu-id="16d35-103">Get enrollment accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16d35-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="16d35-104">SYNTAX</span></span>

### <span data-ttu-id="16d35-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="16d35-105">List (Default)</span></span>
```
Get-AzureRmEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16d35-106">Enda</span><span class="sxs-lookup"><span data-stu-id="16d35-106">Single</span></span>
```
Get-AzureRmEnrollmentAccount -ObjectId <System.String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16d35-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="16d35-107">DESCRIPTION</span></span>
<span data-ttu-id="16d35-108">Cmdleten **Get-AzureRmEnrollmentAccount** hämtar registrerings konton.</span><span class="sxs-lookup"><span data-stu-id="16d35-108">The **Get-AzureRmEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="16d35-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="16d35-109">EXAMPLES</span></span>

### <span data-ttu-id="16d35-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="16d35-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="16d35-111">Skaffa alla tillgängliga registrerings konton.</span><span class="sxs-lookup"><span data-stu-id="16d35-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="16d35-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="16d35-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="16d35-113">Skaffa registrerings kontot med angivet objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="16d35-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="16d35-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="16d35-114">PARAMETERS</span></span>

### <span data-ttu-id="16d35-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16d35-115">-DefaultProfile</span></span>
<span data-ttu-id="16d35-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="16d35-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16d35-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="16d35-117">-ObjectId</span></span>
<span data-ttu-id="16d35-118">ObjectId för ett specifikt registrerings konto att få.</span><span class="sxs-lookup"><span data-stu-id="16d35-118">ObjectId of a specific enrollment account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16d35-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16d35-119">CommonParameters</span></span>
<span data-ttu-id="16d35-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16d35-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16d35-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16d35-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16d35-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="16d35-122">INPUTS</span></span>

### <span data-ttu-id="16d35-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="16d35-123">None</span></span>

## <span data-ttu-id="16d35-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="16d35-124">OUTPUTS</span></span>

### <span data-ttu-id="16d35-125">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Billing. Models. PSEnrollmentAccount, Microsoft. Azure. commands. fakturering, version = 0.14.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="16d35-125">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Billing.Models.PSEnrollmentAccount, Microsoft.Azure.Commands.Billing, Version=0.14.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="16d35-126">Microsoft. Azure. commands. Billing. Models. PSEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="16d35-126">Microsoft.Azure.Commands.Billing.Models.PSEnrollmentAccount</span></span>

## <span data-ttu-id="16d35-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="16d35-127">NOTES</span></span>

## <span data-ttu-id="16d35-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="16d35-128">RELATED LINKS</span></span>

