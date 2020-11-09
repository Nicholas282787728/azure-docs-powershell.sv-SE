---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 74e876621948587c116f435f70315c04b403c2f5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321919"
---
# <span data-ttu-id="558ab-101">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="558ab-101">Remove-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="558ab-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="558ab-102">SYNOPSIS</span></span>
<span data-ttu-id="558ab-103">Tar bort en auktoriseringsprincip.</span><span class="sxs-lookup"><span data-stu-id="558ab-103">Removes an authorization server.</span></span>

## <span data-ttu-id="558ab-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="558ab-104">SYNTAX</span></span>

```
Remove-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="558ab-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="558ab-105">DESCRIPTION</span></span>
<span data-ttu-id="558ab-106">Cmdleten **Remove-AzApiManagementAuthorizationServer** tar bort en Azure API Management Authorization Server.</span><span class="sxs-lookup"><span data-stu-id="558ab-106">The **Remove-AzApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="558ab-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="558ab-107">EXAMPLES</span></span>

### <span data-ttu-id="558ab-108">Exempel 1: ta bort en auktoriseringsregel</span><span class="sxs-lookup"><span data-stu-id="558ab-108">Example 1: Remove an authorization server</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "authserverid" -Force
```

<span data-ttu-id="558ab-109">Det här kommandot tar bort den angivna Server för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="558ab-109">This command removes the specified API Management Authorization Server.</span></span>
<span data-ttu-id="558ab-110">Eftersom *Force* -parametern anges krävs ingen bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="558ab-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="558ab-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="558ab-111">PARAMETERS</span></span>

### <span data-ttu-id="558ab-112">-Kontext</span><span class="sxs-lookup"><span data-stu-id="558ab-112">-Context</span></span>
<span data-ttu-id="558ab-113">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="558ab-113">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="558ab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="558ab-114">-DefaultProfile</span></span>
<span data-ttu-id="558ab-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="558ab-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="558ab-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="558ab-116">-PassThru</span></span>
<span data-ttu-id="558ab-117">passthru</span><span class="sxs-lookup"><span data-stu-id="558ab-117">passthru</span></span>

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

### <span data-ttu-id="558ab-118">-ServerId</span><span class="sxs-lookup"><span data-stu-id="558ab-118">-ServerId</span></span>
<span data-ttu-id="558ab-119">Anger ID för den auktoriseringsprincip som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="558ab-119">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="558ab-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="558ab-120">-Confirm</span></span>
<span data-ttu-id="558ab-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="558ab-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="558ab-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="558ab-122">-WhatIf</span></span>
<span data-ttu-id="558ab-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="558ab-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="558ab-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="558ab-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="558ab-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="558ab-125">CommonParameters</span></span>
<span data-ttu-id="558ab-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="558ab-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="558ab-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="558ab-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="558ab-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="558ab-128">INPUTS</span></span>

### <span data-ttu-id="558ab-129">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="558ab-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="558ab-130">System. String</span><span class="sxs-lookup"><span data-stu-id="558ab-130">System.String</span></span>

### <span data-ttu-id="558ab-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="558ab-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="558ab-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="558ab-132">OUTPUTS</span></span>

### <span data-ttu-id="558ab-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="558ab-133">System.Boolean</span></span>

## <span data-ttu-id="558ab-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="558ab-134">NOTES</span></span>

## <span data-ttu-id="558ab-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="558ab-135">RELATED LINKS</span></span>

[<span data-ttu-id="558ab-136">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="558ab-136">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="558ab-137">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="558ab-137">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="558ab-138">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="558ab-138">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


