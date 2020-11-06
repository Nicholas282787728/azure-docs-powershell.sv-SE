---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
ms.openlocfilehash: 485150470bce308d3ab6d1a9a70eabd887abab09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579123"
---
# <span data-ttu-id="16017-101">Get-AzureRmApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="16017-101">Get-AzureRmApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="16017-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="16017-102">SYNOPSIS</span></span>
<span data-ttu-id="16017-103">Genererar en SSO URL för en användare.</span><span class="sxs-lookup"><span data-stu-id="16017-103">Generates an SSO URL for a user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16017-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="16017-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16017-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="16017-105">DESCRIPTION</span></span>
<span data-ttu-id="16017-106">Cmdleten **Get-AzureRmApiManagementUserSsoUrl** skapar en URL för en användare.</span><span class="sxs-lookup"><span data-stu-id="16017-106">The **Get-AzureRmApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="16017-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="16017-107">EXAMPLES</span></span>

### <span data-ttu-id="16017-108">Exempel 1: Hämta en användares URL för SSO</span><span class="sxs-lookup"><span data-stu-id="16017-108">Example 1: Get a user's SSO URL</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="16017-109">Det här kommandot får en användares URL för SSO.</span><span class="sxs-lookup"><span data-stu-id="16017-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="16017-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="16017-110">PARAMETERS</span></span>

### <span data-ttu-id="16017-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="16017-111">-Context</span></span>
<span data-ttu-id="16017-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="16017-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="16017-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="16017-113">This parameter is required.</span></span>

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

### <span data-ttu-id="16017-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16017-114">-DefaultProfile</span></span>
<span data-ttu-id="16017-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="16017-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16017-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="16017-116">-UserId</span></span>
<span data-ttu-id="16017-117">Anger ett användar-ID.</span><span class="sxs-lookup"><span data-stu-id="16017-117">Specifies a user ID.</span></span>
<span data-ttu-id="16017-118">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="16017-118">This parameter is required.</span></span>

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

### <span data-ttu-id="16017-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16017-119">CommonParameters</span></span>
<span data-ttu-id="16017-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16017-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16017-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16017-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16017-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="16017-122">INPUTS</span></span>

### <span data-ttu-id="16017-123">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="16017-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="16017-124">System. String</span><span class="sxs-lookup"><span data-stu-id="16017-124">System.String</span></span>

## <span data-ttu-id="16017-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="16017-125">OUTPUTS</span></span>

### <span data-ttu-id="16017-126">System. String</span><span class="sxs-lookup"><span data-stu-id="16017-126">System.String</span></span>

## <span data-ttu-id="16017-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="16017-127">NOTES</span></span>

## <span data-ttu-id="16017-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="16017-128">RELATED LINKS</span></span>

[<span data-ttu-id="16017-129">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="16017-129">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


