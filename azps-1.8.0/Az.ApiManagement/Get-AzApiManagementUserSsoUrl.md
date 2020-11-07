---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
ms.openlocfilehash: 2a7a4d602b8e316377496af8ccb9c119338a5c99
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743386"
---
# <span data-ttu-id="ceaf4-101">Get-AzApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="ceaf4-101">Get-AzApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="ceaf4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ceaf4-102">SYNOPSIS</span></span>
<span data-ttu-id="ceaf4-103">Genererar en SSO URL för en användare.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-103">Generates an SSO URL for a user.</span></span>

## <span data-ttu-id="ceaf4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ceaf4-104">SYNTAX</span></span>

```
Get-AzApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ceaf4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ceaf4-105">DESCRIPTION</span></span>
<span data-ttu-id="ceaf4-106">Cmdleten **Get-AzApiManagementUserSsoUrl** skapar en URL för en användare.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-106">The **Get-AzApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="ceaf4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ceaf4-107">EXAMPLES</span></span>

### <span data-ttu-id="ceaf4-108">Exempel 1: Hämta en användares URL för SSO</span><span class="sxs-lookup"><span data-stu-id="ceaf4-108">Example 1: Get a user's SSO URL</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="ceaf4-109">Det här kommandot får en användares URL för SSO.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="ceaf4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ceaf4-110">PARAMETERS</span></span>

### <span data-ttu-id="ceaf4-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="ceaf4-111">-Context</span></span>
<span data-ttu-id="ceaf4-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="ceaf4-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-113">This parameter is required.</span></span>

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

### <span data-ttu-id="ceaf4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceaf4-114">-DefaultProfile</span></span>
<span data-ttu-id="ceaf4-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ceaf4-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="ceaf4-116">-UserId</span></span>
<span data-ttu-id="ceaf4-117">Anger ett användar-ID.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-117">Specifies a user ID.</span></span>
<span data-ttu-id="ceaf4-118">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-118">This parameter is required.</span></span>

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

### <span data-ttu-id="ceaf4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceaf4-119">CommonParameters</span></span>
<span data-ttu-id="ceaf4-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceaf4-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceaf4-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceaf4-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ceaf4-122">INPUTS</span></span>

### <span data-ttu-id="ceaf4-123">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ceaf4-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ceaf4-124">System. String</span><span class="sxs-lookup"><span data-stu-id="ceaf4-124">System.String</span></span>

## <span data-ttu-id="ceaf4-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ceaf4-125">OUTPUTS</span></span>

### <span data-ttu-id="ceaf4-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ceaf4-126">System.String</span></span>

## <span data-ttu-id="ceaf4-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ceaf4-127">NOTES</span></span>

## <span data-ttu-id="ceaf4-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ceaf4-128">RELATED LINKS</span></span>

[<span data-ttu-id="ceaf4-129">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ceaf4-129">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


