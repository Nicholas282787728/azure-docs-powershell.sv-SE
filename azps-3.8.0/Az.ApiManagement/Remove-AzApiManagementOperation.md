---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
ms.openlocfilehash: 153eb354ae8ba0f033a34010658b0d851572ddd6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089877"
---
# <span data-ttu-id="42e21-101">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="42e21-101">Remove-AzApiManagementOperation</span></span>

## <span data-ttu-id="42e21-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="42e21-102">SYNOPSIS</span></span>
<span data-ttu-id="42e21-103">Tar bort en befintlig åtgärd.</span><span class="sxs-lookup"><span data-stu-id="42e21-103">Removes an existing operation.</span></span>

## <span data-ttu-id="42e21-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="42e21-104">SYNTAX</span></span>

```
Remove-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="42e21-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="42e21-105">DESCRIPTION</span></span>
<span data-ttu-id="42e21-106">Cmdleten **Remove-AzApiManagementOperation** tar bort en befintlig åtgärd.</span><span class="sxs-lookup"><span data-stu-id="42e21-106">The **Remove-AzApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="42e21-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="42e21-107">EXAMPLES</span></span>

### <span data-ttu-id="42e21-108">Exempel 1: ta bort en befintlig API-åtgärd</span><span class="sxs-lookup"><span data-stu-id="42e21-108">Example 1: Remove an existing API Operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="42e21-109">Det här kommandot tar bort en befintlig API-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="42e21-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="42e21-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="42e21-110">PARAMETERS</span></span>

### <span data-ttu-id="42e21-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="42e21-111">-ApiId</span></span>
<span data-ttu-id="42e21-112">Anger API-identifierare.</span><span class="sxs-lookup"><span data-stu-id="42e21-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="42e21-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="42e21-113">-ApiRevision</span></span>
<span data-ttu-id="42e21-114">Identifierare för API-revision.</span><span class="sxs-lookup"><span data-stu-id="42e21-114">Identifier of API Revision.</span></span> <span data-ttu-id="42e21-115">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="42e21-115">This parameter is optional.</span></span> <span data-ttu-id="42e21-116">Om inget anges tas åtgärden bort från den för tillfället aktiva API-ändringen.</span><span class="sxs-lookup"><span data-stu-id="42e21-116">If not specified, the operation will be removed from the currently active api revision.</span></span>

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

### <span data-ttu-id="42e21-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="42e21-117">-Context</span></span>
<span data-ttu-id="42e21-118">Anger en instans av **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="42e21-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="42e21-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42e21-119">-DefaultProfile</span></span>
<span data-ttu-id="42e21-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="42e21-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42e21-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="42e21-121">-OperationId</span></span>
<span data-ttu-id="42e21-122">Anger API-funktionens identifierare.</span><span class="sxs-lookup"><span data-stu-id="42e21-122">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="42e21-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42e21-123">-PassThru</span></span>
<span data-ttu-id="42e21-124">Anger att denna cmdlet returnerar ett värde för $True om det lyckas, eller ett $False värde.</span><span class="sxs-lookup"><span data-stu-id="42e21-124">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="42e21-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="42e21-125">-Confirm</span></span>
<span data-ttu-id="42e21-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="42e21-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42e21-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42e21-127">-WhatIf</span></span>
<span data-ttu-id="42e21-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="42e21-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42e21-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="42e21-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42e21-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42e21-130">CommonParameters</span></span>
<span data-ttu-id="42e21-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42e21-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42e21-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42e21-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42e21-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="42e21-133">INPUTS</span></span>

### <span data-ttu-id="42e21-134">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="42e21-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="42e21-135">System. String</span><span class="sxs-lookup"><span data-stu-id="42e21-135">System.String</span></span>

### <span data-ttu-id="42e21-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="42e21-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="42e21-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="42e21-137">OUTPUTS</span></span>

### <span data-ttu-id="42e21-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="42e21-138">System.Boolean</span></span>

## <span data-ttu-id="42e21-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="42e21-139">NOTES</span></span>

## <span data-ttu-id="42e21-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="42e21-140">RELATED LINKS</span></span>

[<span data-ttu-id="42e21-141">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="42e21-141">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="42e21-142">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="42e21-142">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="42e21-143">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="42e21-143">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)

