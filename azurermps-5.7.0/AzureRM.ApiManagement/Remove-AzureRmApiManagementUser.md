---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
ms.openlocfilehash: 5d657610ddce1c0397a5f9e8c11b832b3fcd472b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758354"
---
# <span data-ttu-id="b7197-101">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="b7197-101">Remove-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="b7197-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b7197-102">SYNOPSIS</span></span>
<span data-ttu-id="b7197-103">Tar bort en befintlig användare.</span><span class="sxs-lookup"><span data-stu-id="b7197-103">Deletes an existing user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7197-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b7197-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7197-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b7197-105">DESCRIPTION</span></span>
<span data-ttu-id="b7197-106">Cmdleten **Remove-AzureRmApiManagementUser** tar bort en befintlig användare.</span><span class="sxs-lookup"><span data-stu-id="b7197-106">The **Remove-AzureRmApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="b7197-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b7197-107">EXAMPLES</span></span>

### <span data-ttu-id="b7197-108">Exempel 1: ta bort en användare</span><span class="sxs-lookup"><span data-stu-id="b7197-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="b7197-109">Det här kommandot tar bort en befintlig användare.</span><span class="sxs-lookup"><span data-stu-id="b7197-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="b7197-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b7197-110">PARAMETERS</span></span>

### <span data-ttu-id="b7197-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="b7197-111">-Context</span></span>
<span data-ttu-id="b7197-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b7197-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="b7197-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="b7197-113">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7197-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7197-114">-DefaultProfile</span></span>
<span data-ttu-id="b7197-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b7197-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7197-116">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="b7197-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="b7197-117">Anger om du vill ta bort abonnemang för produkten.</span><span class="sxs-lookup"><span data-stu-id="b7197-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="b7197-118">Om den här parametern inte anges och det finns en prenumeration returnerar denna cmdlet ett undantag.</span><span class="sxs-lookup"><span data-stu-id="b7197-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="b7197-119">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="b7197-119">This parameter is optional.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7197-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7197-120">-PassThru</span></span>
<span data-ttu-id="b7197-121">Anger att den här cmdleten returnerar ett värde för $Ture, om det lyckas eller ett $False värde.</span><span class="sxs-lookup"><span data-stu-id="b7197-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7197-122">-UserId</span><span class="sxs-lookup"><span data-stu-id="b7197-122">-UserId</span></span>
<span data-ttu-id="b7197-123">Anger ID för den användare som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="b7197-123">Specifies the ID of the user to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7197-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b7197-124">-Confirm</span></span>
<span data-ttu-id="b7197-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b7197-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7197-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7197-126">-WhatIf</span></span>
<span data-ttu-id="b7197-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b7197-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7197-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b7197-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7197-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7197-129">CommonParameters</span></span>
<span data-ttu-id="b7197-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7197-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7197-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7197-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7197-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b7197-132">INPUTS</span></span>

### <span data-ttu-id="b7197-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="b7197-133">None</span></span>
<span data-ttu-id="b7197-134">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="b7197-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b7197-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b7197-135">OUTPUTS</span></span>

### <span data-ttu-id="b7197-136">Returtyp</span><span class="sxs-lookup"><span data-stu-id="b7197-136">Boolean</span></span>

## <span data-ttu-id="b7197-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b7197-137">NOTES</span></span>

## <span data-ttu-id="b7197-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b7197-138">RELATED LINKS</span></span>

[<span data-ttu-id="b7197-139">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="b7197-139">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="b7197-140">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="b7197-140">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="b7197-141">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="b7197-141">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


