---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
ms.openlocfilehash: be30497c444d90b9239b5dc3dcd351fbe9a63f0b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525061"
---
# <span data-ttu-id="53c78-101">Get-AzApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="53c78-101">Get-AzApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="53c78-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="53c78-102">SYNOPSIS</span></span>
<span data-ttu-id="53c78-103">Genererar en SSO URL för en användare.</span><span class="sxs-lookup"><span data-stu-id="53c78-103">Generates an SSO URL for a user.</span></span>

## <span data-ttu-id="53c78-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="53c78-104">SYNTAX</span></span>

```
Get-AzApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53c78-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="53c78-105">DESCRIPTION</span></span>
<span data-ttu-id="53c78-106">Cmdleten **Get-AzApiManagementUserSsoUrl** skapar en URL för en användare.</span><span class="sxs-lookup"><span data-stu-id="53c78-106">The **Get-AzApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="53c78-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="53c78-107">EXAMPLES</span></span>

### <span data-ttu-id="53c78-108">Exempel 1: Hämta en användares URL för SSO</span><span class="sxs-lookup"><span data-stu-id="53c78-108">Example 1: Get a user's SSO URL</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="53c78-109">Det här kommandot får en användares URL för SSO.</span><span class="sxs-lookup"><span data-stu-id="53c78-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="53c78-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="53c78-110">PARAMETERS</span></span>

### <span data-ttu-id="53c78-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="53c78-111">-Context</span></span>
<span data-ttu-id="53c78-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="53c78-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="53c78-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="53c78-113">This parameter is required.</span></span>

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

### <span data-ttu-id="53c78-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53c78-114">-DefaultProfile</span></span>
<span data-ttu-id="53c78-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="53c78-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53c78-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="53c78-116">-UserId</span></span>
<span data-ttu-id="53c78-117">Anger ett användar-ID.</span><span class="sxs-lookup"><span data-stu-id="53c78-117">Specifies a user ID.</span></span>
<span data-ttu-id="53c78-118">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="53c78-118">This parameter is required.</span></span>

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

### <span data-ttu-id="53c78-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53c78-119">CommonParameters</span></span>
<span data-ttu-id="53c78-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53c78-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53c78-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53c78-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53c78-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="53c78-122">INPUTS</span></span>

### <span data-ttu-id="53c78-123">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="53c78-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="53c78-124">System. String</span><span class="sxs-lookup"><span data-stu-id="53c78-124">System.String</span></span>

## <span data-ttu-id="53c78-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="53c78-125">OUTPUTS</span></span>

### <span data-ttu-id="53c78-126">System. String</span><span class="sxs-lookup"><span data-stu-id="53c78-126">System.String</span></span>

## <span data-ttu-id="53c78-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="53c78-127">NOTES</span></span>

## <span data-ttu-id="53c78-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="53c78-128">RELATED LINKS</span></span>

[<span data-ttu-id="53c78-129">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="53c78-129">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


