---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
ms.openlocfilehash: 08bbb81998107a11a5996cb75a6fba8b760802db
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260387"
---
# <span data-ttu-id="d9817-101">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="d9817-101">Set-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="d9817-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d9817-102">SYNOPSIS</span></span>
<span data-ttu-id="d9817-103">Aktiverar eller inaktiverar klient åtkomst.</span><span class="sxs-lookup"><span data-stu-id="d9817-103">Enables or disables tenant access.</span></span>

## <span data-ttu-id="d9817-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d9817-104">SYNTAX</span></span>

```
Set-AzApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9817-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d9817-105">DESCRIPTION</span></span>
<span data-ttu-id="d9817-106">Cmdleten **set-AzApiManagementTenantAccess** aktiverar eller inaktiverar klient åtkomst.</span><span class="sxs-lookup"><span data-stu-id="d9817-106">The **Set-AzApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="d9817-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d9817-107">EXAMPLES</span></span>

### <span data-ttu-id="d9817-108">Exempel 1: Aktivera klient åtkomst</span><span class="sxs-lookup"><span data-stu-id="d9817-108">Example 1: Enable tenant access</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementTenantAccess -Context $apimContext -Enabled $True
```

<span data-ttu-id="d9817-109">Det här kommandot aktiverar klient åtkomst i angiven kontext.</span><span class="sxs-lookup"><span data-stu-id="d9817-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="d9817-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d9817-110">PARAMETERS</span></span>

### <span data-ttu-id="d9817-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="d9817-111">-Context</span></span>
<span data-ttu-id="d9817-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d9817-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d9817-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9817-113">-DefaultProfile</span></span>
<span data-ttu-id="d9817-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d9817-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9817-115">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="d9817-115">-Enabled</span></span>
<span data-ttu-id="d9817-116">Anger om denna cmdlet aktiverar eller inaktiverar klient åtkomst.</span><span class="sxs-lookup"><span data-stu-id="d9817-116">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="d9817-117">Ange ett värde för $True som ska aktive ras eller $Falses.</span><span class="sxs-lookup"><span data-stu-id="d9817-117">Specify a value of $True to enable or $False to disable.</span></span>

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

### <span data-ttu-id="d9817-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9817-118">-PassThru</span></span>
<span data-ttu-id="d9817-119">Anger att denna cmdlet returnerar **PsApiManagementAccessInformation** som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="d9817-119">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d9817-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9817-120">CommonParameters</span></span>
<span data-ttu-id="d9817-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9817-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9817-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9817-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9817-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d9817-123">INPUTS</span></span>

### <span data-ttu-id="d9817-124">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d9817-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d9817-125">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d9817-125">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d9817-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d9817-126">OUTPUTS</span></span>

### <span data-ttu-id="d9817-127">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="d9817-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="d9817-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d9817-128">NOTES</span></span>

## <span data-ttu-id="d9817-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d9817-129">RELATED LINKS</span></span>

[<span data-ttu-id="d9817-130">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="d9817-130">Get-AzApiManagementTenantAccess</span></span>](./Get-AzApiManagementTenantAccess.md)

