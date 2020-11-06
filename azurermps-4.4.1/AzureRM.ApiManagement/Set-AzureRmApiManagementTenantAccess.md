---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: c75aceee59e5696d928f19fa6d5ae317828fa82f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573751"
---
# <span data-ttu-id="063cb-101">Set-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="063cb-101">Set-AzureRmApiManagementTenantAccess</span></span>

## <span data-ttu-id="063cb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="063cb-102">SYNOPSIS</span></span>
<span data-ttu-id="063cb-103">Aktiverar eller inaktiverar klient åtkomst.</span><span class="sxs-lookup"><span data-stu-id="063cb-103">Enables or disables tenant access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="063cb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="063cb-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="063cb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="063cb-105">DESCRIPTION</span></span>
<span data-ttu-id="063cb-106">Cmdleten **set-AzureRmApiManagementTenantAccess** aktiverar eller inaktiverar klient åtkomst.</span><span class="sxs-lookup"><span data-stu-id="063cb-106">The **Set-AzureRmApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="063cb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="063cb-107">EXAMPLES</span></span>

### <span data-ttu-id="063cb-108">Exempel 1: Aktivera klient åtkomst</span><span class="sxs-lookup"><span data-stu-id="063cb-108">Example 1: Enable tenant access</span></span>
```
PS C:\>Set-AzureRmApiManagementTenantAccess -Context $ApimContext -Enabled $True
```

<span data-ttu-id="063cb-109">Det här kommandot aktiverar klient åtkomst i angiven kontext.</span><span class="sxs-lookup"><span data-stu-id="063cb-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="063cb-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="063cb-110">PARAMETERS</span></span>

### <span data-ttu-id="063cb-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="063cb-111">-Context</span></span>
<span data-ttu-id="063cb-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="063cb-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="063cb-113">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="063cb-113">-Enabled</span></span>
<span data-ttu-id="063cb-114">Anger om denna cmdlet aktiverar eller inaktiverar klient åtkomst.</span><span class="sxs-lookup"><span data-stu-id="063cb-114">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="063cb-115">Ange ett värde för $True som ska aktive ras eller $Falses.</span><span class="sxs-lookup"><span data-stu-id="063cb-115">Specify a value of $True to enable or $False to disable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="063cb-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="063cb-116">-PassThru</span></span>
<span data-ttu-id="063cb-117">Anger att denna cmdlet returnerar **PsApiManagementAccessInformation** som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="063cb-117">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="063cb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="063cb-118">-DefaultProfile</span></span>
<span data-ttu-id="063cb-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="063cb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="063cb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="063cb-120">CommonParameters</span></span>
<span data-ttu-id="063cb-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="063cb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="063cb-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="063cb-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="063cb-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="063cb-123">INPUTS</span></span>

## <span data-ttu-id="063cb-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="063cb-124">OUTPUTS</span></span>

### <span data-ttu-id="063cb-125">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="063cb-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="063cb-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="063cb-126">NOTES</span></span>

## <span data-ttu-id="063cb-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="063cb-127">RELATED LINKS</span></span>

[<span data-ttu-id="063cb-128">Get-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="063cb-128">Get-AzureRmApiManagementTenantAccess</span></span>](./Get-AzureRmApiManagementTenantAccess.md)


