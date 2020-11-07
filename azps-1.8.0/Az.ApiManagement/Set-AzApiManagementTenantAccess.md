---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
ms.openlocfilehash: 5f14a0698c0b1ea950a28236a8a523734b2ddf5e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917673"
---
# <span data-ttu-id="1525a-101">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="1525a-101">Set-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="1525a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1525a-102">SYNOPSIS</span></span>
<span data-ttu-id="1525a-103">Aktiverar eller inaktiverar klient åtkomst.</span><span class="sxs-lookup"><span data-stu-id="1525a-103">Enables or disables tenant access.</span></span>

## <span data-ttu-id="1525a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1525a-104">SYNTAX</span></span>

```
Set-AzApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1525a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1525a-105">DESCRIPTION</span></span>
<span data-ttu-id="1525a-106">Cmdleten **set-AzApiManagementTenantAccess** aktiverar eller inaktiverar klient åtkomst.</span><span class="sxs-lookup"><span data-stu-id="1525a-106">The **Set-AzApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="1525a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1525a-107">EXAMPLES</span></span>

### <span data-ttu-id="1525a-108">Exempel 1: Aktivera klient åtkomst</span><span class="sxs-lookup"><span data-stu-id="1525a-108">Example 1: Enable tenant access</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementTenantAccess -Context $apimContext -Enabled $True
```

<span data-ttu-id="1525a-109">Det här kommandot aktiverar klient åtkomst i angiven kontext.</span><span class="sxs-lookup"><span data-stu-id="1525a-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="1525a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1525a-110">PARAMETERS</span></span>

### <span data-ttu-id="1525a-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="1525a-111">-Context</span></span>
<span data-ttu-id="1525a-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="1525a-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1525a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1525a-113">-DefaultProfile</span></span>
<span data-ttu-id="1525a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1525a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1525a-115">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="1525a-115">-Enabled</span></span>
<span data-ttu-id="1525a-116">Anger om denna cmdlet aktiverar eller inaktiverar klient åtkomst.</span><span class="sxs-lookup"><span data-stu-id="1525a-116">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="1525a-117">Ange ett värde för $True som ska aktive ras eller $Falses.</span><span class="sxs-lookup"><span data-stu-id="1525a-117">Specify a value of $True to enable or $False to disable.</span></span>

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

### <span data-ttu-id="1525a-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1525a-118">-PassThru</span></span>
<span data-ttu-id="1525a-119">Anger att denna cmdlet returnerar **PsApiManagementAccessInformation** som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="1525a-119">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1525a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1525a-120">CommonParameters</span></span>
<span data-ttu-id="1525a-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1525a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1525a-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1525a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1525a-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1525a-123">INPUTS</span></span>

### <span data-ttu-id="1525a-124">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1525a-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1525a-125">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1525a-125">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1525a-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1525a-126">OUTPUTS</span></span>

### <span data-ttu-id="1525a-127">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="1525a-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="1525a-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1525a-128">NOTES</span></span>

## <span data-ttu-id="1525a-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1525a-129">RELATED LINKS</span></span>

[<span data-ttu-id="1525a-130">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="1525a-130">Get-AzApiManagementTenantAccess</span></span>](./Get-AzApiManagementTenantAccess.md)


