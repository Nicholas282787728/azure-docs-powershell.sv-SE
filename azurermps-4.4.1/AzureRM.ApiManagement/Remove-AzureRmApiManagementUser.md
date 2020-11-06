---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
ms.openlocfilehash: 6be4c714627d77b0e3c56b8dd9766c550deebd7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573752"
---
# <span data-ttu-id="967c5-101">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="967c5-101">Remove-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="967c5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="967c5-102">SYNOPSIS</span></span>
<span data-ttu-id="967c5-103">Tar bort en befintlig användare.</span><span class="sxs-lookup"><span data-stu-id="967c5-103">Deletes an existing user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="967c5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="967c5-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="967c5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="967c5-105">DESCRIPTION</span></span>
<span data-ttu-id="967c5-106">Cmdleten **Remove-AzureRmApiManagementUser** tar bort en befintlig användare.</span><span class="sxs-lookup"><span data-stu-id="967c5-106">The **Remove-AzureRmApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="967c5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="967c5-107">EXAMPLES</span></span>

### <span data-ttu-id="967c5-108">Exempel 1: ta bort en användare</span><span class="sxs-lookup"><span data-stu-id="967c5-108">Example 1: Delete a user</span></span>
```
PS C:\>Remove-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="967c5-109">Det här kommandot tar bort en befintlig användare.</span><span class="sxs-lookup"><span data-stu-id="967c5-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="967c5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="967c5-110">PARAMETERS</span></span>

### <span data-ttu-id="967c5-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="967c5-111">-Context</span></span>
<span data-ttu-id="967c5-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="967c5-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="967c5-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="967c5-113">This parameter is required.</span></span>

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

### <span data-ttu-id="967c5-114">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="967c5-114">-DeleteSubscriptions</span></span>
<span data-ttu-id="967c5-115">Anger om du vill ta bort abonnemang för produkten.</span><span class="sxs-lookup"><span data-stu-id="967c5-115">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="967c5-116">Om den här parametern inte anges och det finns en prenumeration returnerar denna cmdlet ett undantag.</span><span class="sxs-lookup"><span data-stu-id="967c5-116">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="967c5-117">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="967c5-117">This parameter is optional.</span></span>

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

### <span data-ttu-id="967c5-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="967c5-118">-PassThru</span></span>
<span data-ttu-id="967c5-119">Anger att den här cmdleten returnerar ett värde för $Ture, om det lyckas eller ett $False värde.</span><span class="sxs-lookup"><span data-stu-id="967c5-119">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="967c5-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="967c5-120">-UserId</span></span>
<span data-ttu-id="967c5-121">Anger ID för den användare som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="967c5-121">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="967c5-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="967c5-122">-Confirm</span></span>
<span data-ttu-id="967c5-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="967c5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="967c5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="967c5-124">-WhatIf</span></span>
<span data-ttu-id="967c5-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="967c5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="967c5-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="967c5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="967c5-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="967c5-127">-DefaultProfile</span></span>
<span data-ttu-id="967c5-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="967c5-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="967c5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="967c5-129">CommonParameters</span></span>
<span data-ttu-id="967c5-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="967c5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="967c5-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="967c5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="967c5-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="967c5-132">INPUTS</span></span>

## <span data-ttu-id="967c5-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="967c5-133">OUTPUTS</span></span>

### <span data-ttu-id="967c5-134">Returtyp</span><span class="sxs-lookup"><span data-stu-id="967c5-134">Boolean</span></span>

## <span data-ttu-id="967c5-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="967c5-135">NOTES</span></span>

## <span data-ttu-id="967c5-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="967c5-136">RELATED LINKS</span></span>

[<span data-ttu-id="967c5-137">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="967c5-137">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="967c5-138">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="967c5-138">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="967c5-139">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="967c5-139">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


