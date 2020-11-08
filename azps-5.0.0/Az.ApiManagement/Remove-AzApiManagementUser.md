---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
ms.openlocfilehash: 4c90b51a316db63bad2e5481e1b6390849d83292
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269381"
---
# <span data-ttu-id="88ede-101">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="88ede-101">Remove-AzApiManagementUser</span></span>

## <span data-ttu-id="88ede-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="88ede-102">SYNOPSIS</span></span>
<span data-ttu-id="88ede-103">Tar bort en befintlig användare.</span><span class="sxs-lookup"><span data-stu-id="88ede-103">Deletes an existing user.</span></span>

## <span data-ttu-id="88ede-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="88ede-104">SYNTAX</span></span>

```
Remove-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88ede-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="88ede-105">DESCRIPTION</span></span>
<span data-ttu-id="88ede-106">Cmdleten **Remove-AzApiManagementUser** tar bort en befintlig användare.</span><span class="sxs-lookup"><span data-stu-id="88ede-106">The **Remove-AzApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="88ede-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="88ede-107">EXAMPLES</span></span>

### <span data-ttu-id="88ede-108">Exempel 1: ta bort en användare</span><span class="sxs-lookup"><span data-stu-id="88ede-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="88ede-109">Det här kommandot tar bort en befintlig användare.</span><span class="sxs-lookup"><span data-stu-id="88ede-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="88ede-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="88ede-110">PARAMETERS</span></span>

### <span data-ttu-id="88ede-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="88ede-111">-Context</span></span>
<span data-ttu-id="88ede-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="88ede-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="88ede-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="88ede-113">This parameter is required.</span></span>

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

### <span data-ttu-id="88ede-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88ede-114">-DefaultProfile</span></span>
<span data-ttu-id="88ede-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="88ede-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88ede-116">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="88ede-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="88ede-117">Anger om du vill ta bort abonnemang för produkten.</span><span class="sxs-lookup"><span data-stu-id="88ede-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="88ede-118">Om den här parametern inte anges och det finns en prenumeration returnerar denna cmdlet ett undantag.</span><span class="sxs-lookup"><span data-stu-id="88ede-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="88ede-119">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="88ede-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="88ede-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88ede-120">-PassThru</span></span>
<span data-ttu-id="88ede-121">Anger att den här cmdleten returnerar ett värde för $Ture, om det lyckas eller ett $False värde.</span><span class="sxs-lookup"><span data-stu-id="88ede-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="88ede-122">-UserId</span><span class="sxs-lookup"><span data-stu-id="88ede-122">-UserId</span></span>
<span data-ttu-id="88ede-123">Anger ID för den användare som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="88ede-123">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="88ede-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="88ede-124">-Confirm</span></span>
<span data-ttu-id="88ede-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="88ede-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ede-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88ede-126">-WhatIf</span></span>
<span data-ttu-id="88ede-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="88ede-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88ede-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="88ede-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ede-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88ede-129">CommonParameters</span></span>
<span data-ttu-id="88ede-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88ede-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88ede-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88ede-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88ede-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="88ede-132">INPUTS</span></span>

### <span data-ttu-id="88ede-133">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="88ede-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="88ede-134">System. String</span><span class="sxs-lookup"><span data-stu-id="88ede-134">System.String</span></span>

### <span data-ttu-id="88ede-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="88ede-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="88ede-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="88ede-136">OUTPUTS</span></span>

### <span data-ttu-id="88ede-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="88ede-137">System.Boolean</span></span>

## <span data-ttu-id="88ede-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="88ede-138">NOTES</span></span>

## <span data-ttu-id="88ede-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="88ede-139">RELATED LINKS</span></span>

[<span data-ttu-id="88ede-140">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="88ede-140">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="88ede-141">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="88ede-141">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="88ede-142">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="88ede-142">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


