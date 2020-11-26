---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: c0c659f195aa1104b14f41e4cbc82a1ad86a1b1f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323460"
---
# <span data-ttu-id="2eed8-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="2eed8-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="2eed8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2eed8-102">SYNOPSIS</span></span>
<span data-ttu-id="2eed8-103">Hämtar åtkomst konfigurationen för en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="2eed8-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="2eed8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2eed8-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2eed8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2eed8-105">DESCRIPTION</span></span>
<span data-ttu-id="2eed8-106">Cmdleten **Get-AzApiManagementTenantAccess** hämtar klient åtkomst konfigurationen för en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="2eed8-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>
<span data-ttu-id="2eed8-107">Nycklarna tas inte med i resultatet.</span><span class="sxs-lookup"><span data-stu-id="2eed8-107">Keys will not be included into result details.</span></span> <span data-ttu-id="2eed8-108">Använd **Get-AzApiManagementTenantAccessSecret** för att få klient hemlighet.</span><span class="sxs-lookup"><span data-stu-id="2eed8-108">To get client secret, use **Get-AzApiManagementTenantAccessSecret**.</span></span>

## <span data-ttu-id="2eed8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2eed8-109">EXAMPLES</span></span>

### <span data-ttu-id="2eed8-110">Exempel 1: Hämta konfiguration för klient åtkomst</span><span class="sxs-lookup"><span data-stu-id="2eed8-110">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="2eed8-111">Det här kommandot får klient åtkomst konfigurationen för angiven kontext.</span><span class="sxs-lookup"><span data-stu-id="2eed8-111">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="2eed8-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2eed8-112">PARAMETERS</span></span>

### <span data-ttu-id="2eed8-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="2eed8-113">-Context</span></span>
<span data-ttu-id="2eed8-114">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="2eed8-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2eed8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eed8-115">-DefaultProfile</span></span>
<span data-ttu-id="2eed8-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2eed8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2eed8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eed8-117">CommonParameters</span></span>
<span data-ttu-id="2eed8-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eed8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eed8-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2eed8-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eed8-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2eed8-120">INPUTS</span></span>

### <span data-ttu-id="2eed8-121">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2eed8-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="2eed8-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2eed8-122">OUTPUTS</span></span>

### <span data-ttu-id="2eed8-123">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="2eed8-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="2eed8-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2eed8-124">NOTES</span></span>

## <span data-ttu-id="2eed8-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2eed8-125">RELATED LINKS</span></span>

[<span data-ttu-id="2eed8-126">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="2eed8-126">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)

