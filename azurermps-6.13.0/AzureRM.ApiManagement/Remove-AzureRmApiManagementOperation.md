---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
ms.openlocfilehash: 1a3fd2ca25099be029616e048c5ebfa0e398229e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573040"
---
# <span data-ttu-id="ed990-101">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ed990-101">Remove-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="ed990-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed990-102">SYNOPSIS</span></span>
<span data-ttu-id="ed990-103">Tar bort en befintlig åtgärd.</span><span class="sxs-lookup"><span data-stu-id="ed990-103">Removes an existing operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed990-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed990-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ed990-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed990-105">DESCRIPTION</span></span>
<span data-ttu-id="ed990-106">Cmdleten **Remove-AzureRmApiManagementOperation** tar bort en befintlig åtgärd.</span><span class="sxs-lookup"><span data-stu-id="ed990-106">The **Remove-AzureRmApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="ed990-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed990-107">EXAMPLES</span></span>

### <span data-ttu-id="ed990-108">Exempel 1: ta bort en befintlig API-åtgärd</span><span class="sxs-lookup"><span data-stu-id="ed990-108">Example 1: Remove an existing API Operation</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="ed990-109">Det här kommandot tar bort en befintlig API-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="ed990-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="ed990-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed990-110">PARAMETERS</span></span>

### <span data-ttu-id="ed990-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ed990-111">-ApiId</span></span>
<span data-ttu-id="ed990-112">Anger API-identifierare.</span><span class="sxs-lookup"><span data-stu-id="ed990-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="ed990-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="ed990-113">-ApiRevision</span></span>
<span data-ttu-id="ed990-114">Identifierare för API-revision.</span><span class="sxs-lookup"><span data-stu-id="ed990-114">Identifier of API Revision.</span></span> <span data-ttu-id="ed990-115">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="ed990-115">This parameter is optional.</span></span> <span data-ttu-id="ed990-116">Om inget anges tas åtgärden bort från den för tillfället aktiva API-ändringen.</span><span class="sxs-lookup"><span data-stu-id="ed990-116">If not specified, the operation will be removed from the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed990-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="ed990-117">-Context</span></span>
<span data-ttu-id="ed990-118">Anger en instans av **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="ed990-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="ed990-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed990-119">-DefaultProfile</span></span>
<span data-ttu-id="ed990-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ed990-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed990-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="ed990-121">-OperationId</span></span>
<span data-ttu-id="ed990-122">Anger API-funktionens identifierare.</span><span class="sxs-lookup"><span data-stu-id="ed990-122">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="ed990-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed990-123">-PassThru</span></span>
<span data-ttu-id="ed990-124">Anger att denna cmdlet returnerar ett värde för $True om det lyckas, eller ett $False värde.</span><span class="sxs-lookup"><span data-stu-id="ed990-124">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="ed990-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ed990-125">-Confirm</span></span>
<span data-ttu-id="ed990-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ed990-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed990-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed990-127">-WhatIf</span></span>
<span data-ttu-id="ed990-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ed990-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed990-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ed990-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed990-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed990-130">CommonParameters</span></span>
<span data-ttu-id="ed990-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed990-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed990-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed990-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed990-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed990-133">INPUTS</span></span>

### <span data-ttu-id="ed990-134">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ed990-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ed990-135">System. String</span><span class="sxs-lookup"><span data-stu-id="ed990-135">System.String</span></span>

### <span data-ttu-id="ed990-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ed990-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ed990-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed990-137">OUTPUTS</span></span>

### <span data-ttu-id="ed990-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ed990-138">System.Boolean</span></span>

## <span data-ttu-id="ed990-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed990-139">NOTES</span></span>

## <span data-ttu-id="ed990-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed990-140">RELATED LINKS</span></span>

[<span data-ttu-id="ed990-141">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ed990-141">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="ed990-142">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ed990-142">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="ed990-143">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ed990-143">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


