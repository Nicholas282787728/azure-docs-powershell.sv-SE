---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
ms.openlocfilehash: a13d37100e553d8d56cf5b040a796adabe08b7d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578672"
---
# <span data-ttu-id="0a146-101">Get-AzureRmApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="0a146-101">Get-AzureRmApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="0a146-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0a146-102">SYNOPSIS</span></span>
<span data-ttu-id="0a146-103">Genererar en SSO URL för en användare.</span><span class="sxs-lookup"><span data-stu-id="0a146-103">Generates an SSO URL for a user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a146-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0a146-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a146-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0a146-105">DESCRIPTION</span></span>
<span data-ttu-id="0a146-106">Cmdleten **Get-AzureRmApiManagementUserSsoUrl** skapar en URL för en användare.</span><span class="sxs-lookup"><span data-stu-id="0a146-106">The **Get-AzureRmApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="0a146-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0a146-107">EXAMPLES</span></span>

### <span data-ttu-id="0a146-108">Exempel 1: Hämta en användares URL för SSO</span><span class="sxs-lookup"><span data-stu-id="0a146-108">Example 1: Get a user's SSO URL</span></span>
```
PS C:\>Get-AzureRmApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="0a146-109">Det här kommandot får en användares URL för SSO.</span><span class="sxs-lookup"><span data-stu-id="0a146-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="0a146-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0a146-110">PARAMETERS</span></span>

### <span data-ttu-id="0a146-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="0a146-111">-Context</span></span>
<span data-ttu-id="0a146-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="0a146-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="0a146-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="0a146-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a146-114">-UserId</span><span class="sxs-lookup"><span data-stu-id="0a146-114">-UserId</span></span>
<span data-ttu-id="0a146-115">Anger ett användar-ID.</span><span class="sxs-lookup"><span data-stu-id="0a146-115">Specifies a user ID.</span></span>
<span data-ttu-id="0a146-116">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="0a146-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a146-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a146-117">-DefaultProfile</span></span>
<span data-ttu-id="0a146-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0a146-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a146-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a146-119">CommonParameters</span></span>
<span data-ttu-id="0a146-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a146-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a146-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a146-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a146-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0a146-122">INPUTS</span></span>

## <span data-ttu-id="0a146-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0a146-123">OUTPUTS</span></span>

### <span data-ttu-id="0a146-124">strängvärdet</span><span class="sxs-lookup"><span data-stu-id="0a146-124">string</span></span>

## <span data-ttu-id="0a146-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0a146-125">NOTES</span></span>

## <span data-ttu-id="0a146-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0a146-126">RELATED LINKS</span></span>

[<span data-ttu-id="0a146-127">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="0a146-127">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


