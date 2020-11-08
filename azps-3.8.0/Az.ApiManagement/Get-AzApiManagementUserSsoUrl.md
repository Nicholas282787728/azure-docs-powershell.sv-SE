---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
ms.openlocfilehash: be30497c444d90b9239b5dc3dcd351fbe9a63f0b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090574"
---
# <span data-ttu-id="f035d-101">Get-AzApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="f035d-101">Get-AzApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="f035d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f035d-102">SYNOPSIS</span></span>
<span data-ttu-id="f035d-103">Genererar en SSO URL för en användare.</span><span class="sxs-lookup"><span data-stu-id="f035d-103">Generates an SSO URL for a user.</span></span>

## <span data-ttu-id="f035d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f035d-104">SYNTAX</span></span>

```
Get-AzApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f035d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f035d-105">DESCRIPTION</span></span>
<span data-ttu-id="f035d-106">Cmdleten **Get-AzApiManagementUserSsoUrl** skapar en URL för en användare.</span><span class="sxs-lookup"><span data-stu-id="f035d-106">The **Get-AzApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="f035d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f035d-107">EXAMPLES</span></span>

### <span data-ttu-id="f035d-108">Exempel 1: Hämta en användares URL för SSO</span><span class="sxs-lookup"><span data-stu-id="f035d-108">Example 1: Get a user's SSO URL</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="f035d-109">Det här kommandot får en användares URL för SSO.</span><span class="sxs-lookup"><span data-stu-id="f035d-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="f035d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f035d-110">PARAMETERS</span></span>

### <span data-ttu-id="f035d-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="f035d-111">-Context</span></span>
<span data-ttu-id="f035d-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="f035d-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="f035d-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="f035d-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f035d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f035d-114">-DefaultProfile</span></span>
<span data-ttu-id="f035d-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f035d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f035d-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="f035d-116">-UserId</span></span>
<span data-ttu-id="f035d-117">Anger ett användar-ID.</span><span class="sxs-lookup"><span data-stu-id="f035d-117">Specifies a user ID.</span></span>
<span data-ttu-id="f035d-118">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="f035d-118">This parameter is required.</span></span>

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

### <span data-ttu-id="f035d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f035d-119">CommonParameters</span></span>
<span data-ttu-id="f035d-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f035d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f035d-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f035d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f035d-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f035d-122">INPUTS</span></span>

### <span data-ttu-id="f035d-123">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f035d-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f035d-124">System. String</span><span class="sxs-lookup"><span data-stu-id="f035d-124">System.String</span></span>

## <span data-ttu-id="f035d-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f035d-125">OUTPUTS</span></span>

### <span data-ttu-id="f035d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f035d-126">System.String</span></span>

## <span data-ttu-id="f035d-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f035d-127">NOTES</span></span>

## <span data-ttu-id="f035d-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f035d-128">RELATED LINKS</span></span>

[<span data-ttu-id="f035d-129">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f035d-129">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

