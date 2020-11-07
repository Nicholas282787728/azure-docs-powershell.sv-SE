---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 41266c660a7dde6064b7f57e3f0303359bba6a8e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745727"
---
# <span data-ttu-id="c3f3d-101">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="c3f3d-101">Remove-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="c3f3d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c3f3d-102">SYNOPSIS</span></span>
<span data-ttu-id="c3f3d-103">Tar bort en auktoriseringsprincip.</span><span class="sxs-lookup"><span data-stu-id="c3f3d-103">Removes an authorization server.</span></span>

## <span data-ttu-id="c3f3d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c3f3d-104">SYNTAX</span></span>

```
Remove-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3f3d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c3f3d-105">DESCRIPTION</span></span>
<span data-ttu-id="c3f3d-106">Cmdleten **Remove-AzApiManagementAuthorizationServer** tar bort en Azure API Management Authorization Server.</span><span class="sxs-lookup"><span data-stu-id="c3f3d-106">The **Remove-AzApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="c3f3d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c3f3d-107">EXAMPLES</span></span>

### <span data-ttu-id="c3f3d-108">Exempel 1: ta bort en auktoriseringsregel</span><span class="sxs-lookup"><span data-stu-id="c3f3d-108">Example 1: Remove an authorization server</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "authserverid" -Force
```

<span data-ttu-id="c3f3d-109">Det här kommandot tar bort den angivna Server för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="c3f3d-109">This command removes the specified API Management Authorization Server.</span></span>
<span data-ttu-id="c3f3d-110">Eftersom *Force* -parametern anges krävs ingen bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c3f3d-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="c3f3d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c3f3d-111">PARAMETERS</span></span>

### <span data-ttu-id="c3f3d-112">-Kontext</span><span class="sxs-lookup"><span data-stu-id="c3f3d-112">-Context</span></span>
<span data-ttu-id="c3f3d-113">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="c3f3d-113">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c3f3d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3f3d-114">-DefaultProfile</span></span>
<span data-ttu-id="c3f3d-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c3f3d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3f3d-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3f3d-116">-PassThru</span></span>
<span data-ttu-id="c3f3d-117">passthru</span><span class="sxs-lookup"><span data-stu-id="c3f3d-117">passthru</span></span>

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

### <span data-ttu-id="c3f3d-118">-ServerId</span><span class="sxs-lookup"><span data-stu-id="c3f3d-118">-ServerId</span></span>
<span data-ttu-id="c3f3d-119">Anger ID för den auktoriseringsprincip som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="c3f3d-119">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="c3f3d-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c3f3d-120">-Confirm</span></span>
<span data-ttu-id="c3f3d-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c3f3d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3f3d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3f3d-122">-WhatIf</span></span>
<span data-ttu-id="c3f3d-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c3f3d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3f3d-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c3f3d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3f3d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3f3d-125">CommonParameters</span></span>
<span data-ttu-id="c3f3d-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3f3d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3f3d-127">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3f3d-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3f3d-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c3f3d-128">INPUTS</span></span>

### <span data-ttu-id="c3f3d-129">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c3f3d-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c3f3d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c3f3d-130">System.String</span></span>

### <span data-ttu-id="c3f3d-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c3f3d-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c3f3d-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c3f3d-132">OUTPUTS</span></span>

### <span data-ttu-id="c3f3d-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c3f3d-133">System.Boolean</span></span>

## <span data-ttu-id="c3f3d-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c3f3d-134">NOTES</span></span>

## <span data-ttu-id="c3f3d-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c3f3d-135">RELATED LINKS</span></span>

[<span data-ttu-id="c3f3d-136">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="c3f3d-136">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="c3f3d-137">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="c3f3d-137">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="c3f3d-138">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="c3f3d-138">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


