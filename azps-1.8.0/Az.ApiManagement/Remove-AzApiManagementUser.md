---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
ms.openlocfilehash: c8c4a318f3d2e972e742afcbdc13350a0ff77a90
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917741"
---
# <span data-ttu-id="d2209-101">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="d2209-101">Remove-AzApiManagementUser</span></span>

## <span data-ttu-id="d2209-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d2209-102">SYNOPSIS</span></span>
<span data-ttu-id="d2209-103">Tar bort en befintlig användare.</span><span class="sxs-lookup"><span data-stu-id="d2209-103">Deletes an existing user.</span></span>

## <span data-ttu-id="d2209-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d2209-104">SYNTAX</span></span>

```
Remove-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2209-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d2209-105">DESCRIPTION</span></span>
<span data-ttu-id="d2209-106">Cmdleten **Remove-AzApiManagementUser** tar bort en befintlig användare.</span><span class="sxs-lookup"><span data-stu-id="d2209-106">The **Remove-AzApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="d2209-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d2209-107">EXAMPLES</span></span>

### <span data-ttu-id="d2209-108">Exempel 1: ta bort en användare</span><span class="sxs-lookup"><span data-stu-id="d2209-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="d2209-109">Det här kommandot tar bort en befintlig användare.</span><span class="sxs-lookup"><span data-stu-id="d2209-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="d2209-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d2209-110">PARAMETERS</span></span>

### <span data-ttu-id="d2209-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="d2209-111">-Context</span></span>
<span data-ttu-id="d2209-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d2209-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="d2209-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="d2209-113">This parameter is required.</span></span>

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

### <span data-ttu-id="d2209-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2209-114">-DefaultProfile</span></span>
<span data-ttu-id="d2209-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d2209-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2209-116">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="d2209-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="d2209-117">Anger om du vill ta bort abonnemang för produkten.</span><span class="sxs-lookup"><span data-stu-id="d2209-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="d2209-118">Om den här parametern inte anges och det finns en prenumeration returnerar denna cmdlet ett undantag.</span><span class="sxs-lookup"><span data-stu-id="d2209-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="d2209-119">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="d2209-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="d2209-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2209-120">-PassThru</span></span>
<span data-ttu-id="d2209-121">Anger att den här cmdleten returnerar ett värde för $Ture, om det lyckas eller ett $False värde.</span><span class="sxs-lookup"><span data-stu-id="d2209-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="d2209-122">-UserId</span><span class="sxs-lookup"><span data-stu-id="d2209-122">-UserId</span></span>
<span data-ttu-id="d2209-123">Anger ID för den användare som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="d2209-123">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="d2209-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d2209-124">-Confirm</span></span>
<span data-ttu-id="d2209-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d2209-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2209-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2209-126">-WhatIf</span></span>
<span data-ttu-id="d2209-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d2209-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2209-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d2209-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2209-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2209-129">CommonParameters</span></span>
<span data-ttu-id="d2209-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2209-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2209-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2209-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2209-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d2209-132">INPUTS</span></span>

### <span data-ttu-id="d2209-133">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d2209-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d2209-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d2209-134">System.String</span></span>

### <span data-ttu-id="d2209-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d2209-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d2209-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d2209-136">OUTPUTS</span></span>

### <span data-ttu-id="d2209-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d2209-137">System.Boolean</span></span>

## <span data-ttu-id="d2209-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d2209-138">NOTES</span></span>

## <span data-ttu-id="d2209-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d2209-139">RELATED LINKS</span></span>

[<span data-ttu-id="d2209-140">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="d2209-140">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="d2209-141">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="d2209-141">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="d2209-142">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="d2209-142">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)

