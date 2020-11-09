---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
ms.openlocfilehash: 27e6be451d6141e322c47b2a84a28baf115839ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321979"
---
# <span data-ttu-id="55728-101">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="55728-101">Add-AzApiManagementUserToGroup</span></span>

## <span data-ttu-id="55728-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="55728-102">SYNOPSIS</span></span>
<span data-ttu-id="55728-103">Lägger till en användare i en grupp.</span><span class="sxs-lookup"><span data-stu-id="55728-103">Adds a user to a group.</span></span>

## <span data-ttu-id="55728-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="55728-104">SYNTAX</span></span>

```
Add-AzApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55728-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="55728-105">DESCRIPTION</span></span>
<span data-ttu-id="55728-106">Cmdleten **Add-AzApiManagementUserToGroup** lägger till en användare i en grupp.</span><span class="sxs-lookup"><span data-stu-id="55728-106">The **Add-AzApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="55728-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="55728-107">EXAMPLES</span></span>

### <span data-ttu-id="55728-108">Exempel 1: lägga till en användare i en grupp</span><span class="sxs-lookup"><span data-stu-id="55728-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="55728-109">Det här kommandot lägger till en befintlig användare i en befintlig grupp.</span><span class="sxs-lookup"><span data-stu-id="55728-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="55728-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="55728-110">PARAMETERS</span></span>

### <span data-ttu-id="55728-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="55728-111">-Context</span></span>
<span data-ttu-id="55728-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="55728-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="55728-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="55728-113">This parameter is required.</span></span>

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

### <span data-ttu-id="55728-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55728-114">-DefaultProfile</span></span>
<span data-ttu-id="55728-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="55728-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55728-116">-Kund-</span><span class="sxs-lookup"><span data-stu-id="55728-116">-GroupId</span></span>
<span data-ttu-id="55728-117">Anger grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="55728-117">Specifies the group ID.</span></span>
<span data-ttu-id="55728-118">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="55728-118">This parameter is required.</span></span>

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

### <span data-ttu-id="55728-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55728-119">-PassThru</span></span>
<span data-ttu-id="55728-120">passthru</span><span class="sxs-lookup"><span data-stu-id="55728-120">passthru</span></span>

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

### <span data-ttu-id="55728-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="55728-121">-UserId</span></span>
<span data-ttu-id="55728-122">Anger användar-ID.</span><span class="sxs-lookup"><span data-stu-id="55728-122">Specifies the user ID.</span></span>
<span data-ttu-id="55728-123">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="55728-123">This parameter is required.</span></span>

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

### <span data-ttu-id="55728-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55728-124">CommonParameters</span></span>
<span data-ttu-id="55728-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55728-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55728-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55728-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55728-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="55728-127">INPUTS</span></span>

### <span data-ttu-id="55728-128">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="55728-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="55728-129">System. String</span><span class="sxs-lookup"><span data-stu-id="55728-129">System.String</span></span>

### <span data-ttu-id="55728-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="55728-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="55728-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="55728-131">OUTPUTS</span></span>

### <span data-ttu-id="55728-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="55728-132">System.Boolean</span></span>

## <span data-ttu-id="55728-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="55728-133">NOTES</span></span>

## <span data-ttu-id="55728-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="55728-134">RELATED LINKS</span></span>

[<span data-ttu-id="55728-135">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="55728-135">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="55728-136">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="55728-136">Remove-AzApiManagementUserFromGroup</span></span>](./Remove-AzApiManagementUserFromGroup.md)


