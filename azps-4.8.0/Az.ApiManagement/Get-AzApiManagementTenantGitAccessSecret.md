---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
ms.openlocfilehash: 51aea46ea65081dd63a3f9f9de4a3a80f4ae8986
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103354"
---
# <span data-ttu-id="d6894-101">Get-AzApiManagementTenantGitAccessSecret</span><span class="sxs-lookup"><span data-stu-id="d6894-101">Get-AzApiManagementTenantGitAccessSecret</span></span>

## <span data-ttu-id="d6894-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d6894-102">SYNOPSIS</span></span>
<span data-ttu-id="d6894-103">Hämtar inställningar för git-åtkomst för en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="d6894-103">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="d6894-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d6894-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6894-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d6894-105">DESCRIPTION</span></span>
<span data-ttu-id="d6894-106">Hämtar inställningar för git-åtkomst för en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="d6894-106">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="d6894-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d6894-107">EXAMPLES</span></span>

### <span data-ttu-id="d6894-108">Exempel 1: Hämta konfiguration för klient åtkomst</span><span class="sxs-lookup"><span data-stu-id="d6894-108">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccessSecret -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="d6894-109">Det här kommandot hämtar konfigurations nycklarna för git-åtkomst för angiven kontext.</span><span class="sxs-lookup"><span data-stu-id="d6894-109">This command gets the Git access configuration keys for the specified context.</span></span>

## <span data-ttu-id="d6894-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d6894-110">PARAMETERS</span></span>

### <span data-ttu-id="d6894-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="d6894-111">-Context</span></span>
<span data-ttu-id="d6894-112">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d6894-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d6894-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="d6894-113">This parameter is required.</span></span>

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

### <span data-ttu-id="d6894-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6894-114">-DefaultProfile</span></span>
<span data-ttu-id="d6894-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d6894-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6894-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6894-116">CommonParameters</span></span>
<span data-ttu-id="d6894-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6894-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6894-118">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6894-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6894-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d6894-119">INPUTS</span></span>

### <span data-ttu-id="d6894-120">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d6894-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="d6894-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d6894-121">OUTPUTS</span></span>

### <span data-ttu-id="d6894-122">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="d6894-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="d6894-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d6894-123">NOTES</span></span>

## <span data-ttu-id="d6894-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d6894-124">RELATED LINKS</span></span>
