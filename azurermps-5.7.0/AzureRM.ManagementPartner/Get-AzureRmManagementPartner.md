---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/get-azurermmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Get-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Get-AzureRmManagementPartner.md
ms.openlocfilehash: b1fe94533074860a3c95c05d6609bb8ebb446a9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578171"
---
# <span data-ttu-id="30e7a-101">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="30e7a-101">Get-AzureRmManagementPartner</span></span>

## <span data-ttu-id="30e7a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="30e7a-102">SYNOPSIS</span></span>
<span data-ttu-id="30e7a-103">Hämtar MPN-ID för den aktuella autentiserade användaren eller tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="30e7a-103">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30e7a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="30e7a-104">SYNTAX</span></span>

```
Get-AzureRmManagementPartner [[-PartnerId] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="30e7a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="30e7a-105">DESCRIPTION</span></span>
<span data-ttu-id="30e7a-106">Hämtar MPN-ID för den aktuella autentiserade användaren eller tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="30e7a-106">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span> 

## <span data-ttu-id="30e7a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="30e7a-107">EXAMPLES</span></span>

### <span data-ttu-id="30e7a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="30e7a-108">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmManagementPartner
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="30e7a-109">Skaffa aktuellt Management partner-ID</span><span class="sxs-lookup"><span data-stu-id="30e7a-109">Get the current management partner id</span></span>

### <span data-ttu-id="30e7a-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="30e7a-110">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="30e7a-111">Skaffa det aktuella Management partner-ID: t med ett partner-ID, om de inte stämmer överens</span><span class="sxs-lookup"><span data-stu-id="30e7a-111">Get the current management partner id using a partner id, if they don't match, it will fail</span></span>

## <span data-ttu-id="30e7a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="30e7a-112">PARAMETERS</span></span>

### <span data-ttu-id="30e7a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30e7a-113">-DefaultProfile</span></span>
<span data-ttu-id="30e7a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="30e7a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30e7a-115">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="30e7a-115">-PartnerId</span></span>
<span data-ttu-id="30e7a-116">ID för hanterings partnern är det ett 6 siffrors nummer</span><span class="sxs-lookup"><span data-stu-id="30e7a-116">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30e7a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30e7a-117">CommonParameters</span></span>
<span data-ttu-id="30e7a-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30e7a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30e7a-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30e7a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30e7a-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="30e7a-120">INPUTS</span></span>

### <span data-ttu-id="30e7a-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="30e7a-121">None</span></span>

## <span data-ttu-id="30e7a-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="30e7a-122">OUTPUTS</span></span>

### <span data-ttu-id="30e7a-123">Microsoft. Azure. commands. Resources. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="30e7a-123">Microsoft.Azure.Commands.Resources.PSManagementPartner</span></span>

## <span data-ttu-id="30e7a-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="30e7a-124">NOTES</span></span>

## <span data-ttu-id="30e7a-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="30e7a-125">RELATED LINKS</span></span>

[<span data-ttu-id="30e7a-126">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="30e7a-126">Remove-AzureRmManagementPartner</span></span>](./Remove-AzureRmManagementPartner.md)

[<span data-ttu-id="30e7a-127">New-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="30e7a-127">New-AzureRmManagementPartner</span></span>](./New-AzureRmManagementPartner.md)

[<span data-ttu-id="30e7a-128">Update-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="30e7a-128">Update-AzureRmManagementPartner</span></span>](./Update-AzureRmManagementPartner.md)
