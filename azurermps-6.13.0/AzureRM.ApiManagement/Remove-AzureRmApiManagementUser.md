---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
ms.openlocfilehash: 31ab005953ea405dc8aac093f973a6e842974814
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581819"
---
# <span data-ttu-id="089a4-101">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="089a4-101">Remove-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="089a4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="089a4-102">SYNOPSIS</span></span>
<span data-ttu-id="089a4-103">Tar bort en befintlig användare.</span><span class="sxs-lookup"><span data-stu-id="089a4-103">Deletes an existing user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="089a4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="089a4-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="089a4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="089a4-105">DESCRIPTION</span></span>
<span data-ttu-id="089a4-106">Cmdleten **Remove-AzureRmApiManagementUser** tar bort en befintlig användare.</span><span class="sxs-lookup"><span data-stu-id="089a4-106">The **Remove-AzureRmApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="089a4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="089a4-107">EXAMPLES</span></span>

### <span data-ttu-id="089a4-108">Exempel 1: ta bort en användare</span><span class="sxs-lookup"><span data-stu-id="089a4-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="089a4-109">Det här kommandot tar bort en befintlig användare.</span><span class="sxs-lookup"><span data-stu-id="089a4-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="089a4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="089a4-110">PARAMETERS</span></span>

### <span data-ttu-id="089a4-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="089a4-111">-Context</span></span>
<span data-ttu-id="089a4-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="089a4-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="089a4-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="089a4-113">This parameter is required.</span></span>

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

### <span data-ttu-id="089a4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="089a4-114">-DefaultProfile</span></span>
<span data-ttu-id="089a4-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="089a4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="089a4-116">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="089a4-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="089a4-117">Anger om du vill ta bort abonnemang för produkten.</span><span class="sxs-lookup"><span data-stu-id="089a4-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="089a4-118">Om den här parametern inte anges och det finns en prenumeration returnerar denna cmdlet ett undantag.</span><span class="sxs-lookup"><span data-stu-id="089a4-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="089a4-119">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="089a4-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="089a4-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="089a4-120">-PassThru</span></span>
<span data-ttu-id="089a4-121">Anger att den här cmdleten returnerar ett värde för $Ture, om det lyckas eller ett $False värde.</span><span class="sxs-lookup"><span data-stu-id="089a4-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="089a4-122">-UserId</span><span class="sxs-lookup"><span data-stu-id="089a4-122">-UserId</span></span>
<span data-ttu-id="089a4-123">Anger ID för den användare som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="089a4-123">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="089a4-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="089a4-124">-Confirm</span></span>
<span data-ttu-id="089a4-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="089a4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="089a4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="089a4-126">-WhatIf</span></span>
<span data-ttu-id="089a4-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="089a4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="089a4-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="089a4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="089a4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="089a4-129">CommonParameters</span></span>
<span data-ttu-id="089a4-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="089a4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="089a4-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="089a4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="089a4-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="089a4-132">INPUTS</span></span>

### <span data-ttu-id="089a4-133">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="089a4-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="089a4-134">System. String</span><span class="sxs-lookup"><span data-stu-id="089a4-134">System.String</span></span>

### <span data-ttu-id="089a4-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="089a4-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="089a4-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="089a4-136">OUTPUTS</span></span>

### <span data-ttu-id="089a4-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="089a4-137">System.Boolean</span></span>

## <span data-ttu-id="089a4-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="089a4-138">NOTES</span></span>

## <span data-ttu-id="089a4-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="089a4-139">RELATED LINKS</span></span>

[<span data-ttu-id="089a4-140">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="089a4-140">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="089a4-141">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="089a4-141">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="089a4-142">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="089a4-142">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


