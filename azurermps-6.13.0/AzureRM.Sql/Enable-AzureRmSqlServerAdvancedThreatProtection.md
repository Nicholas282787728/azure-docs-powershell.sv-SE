---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/enable-azurermsqlserveradvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Enable-AzureRmSqlServerAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Enable-AzureRmSqlServerAdvancedThreatProtection.md
ms.openlocfilehash: 1276ba100a795ca113f1f09064bc46dfdfddf39b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757343"
---
# <span data-ttu-id="df4bf-101">Enable-AzureRmSqlServerAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="df4bf-101">Enable-AzureRmSqlServerAdvancedThreatProtection</span></span>

## <span data-ttu-id="df4bf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="df4bf-102">SYNOPSIS</span></span>
<span data-ttu-id="df4bf-103">Aktiverar Avancerat skydd på en server.</span><span class="sxs-lookup"><span data-stu-id="df4bf-103">Enables Advanced Threat Protection on a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df4bf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="df4bf-104">SYNTAX</span></span>

```
Enable-AzureRmSqlServerAdvancedThreatProtection [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df4bf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="df4bf-105">DESCRIPTION</span></span>
<span data-ttu-id="df4bf-106">Cmdleten **Enable-AzureRmSqlServerAdvancedThreatProtection** aktiverar Avancerat skydd på en server.</span><span class="sxs-lookup"><span data-stu-id="df4bf-106">The **Enable-AzureRmSqlServerAdvancedThreatProtection** cmdlet enables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="df4bf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="df4bf-107">EXAMPLES</span></span>

### <span data-ttu-id="df4bf-108">Exempel 1-aktivera avancerat skydd för Server</span><span class="sxs-lookup"><span data-stu-id="df4bf-108">Example 1 - Enable server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Enable-AzureRmSqlServerAdvancedThreatProtection `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="df4bf-109">Exempel 2 – Aktivera server Avancerat skydd från Server resurs</span><span class="sxs-lookup"><span data-stu-id="df4bf-109">Example 2 - Enable server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzureRmSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Enable-AzureRmSqlServerAdvancedThreatProtection

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="df4bf-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="df4bf-110">PARAMETERS</span></span>

### <span data-ttu-id="df4bf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df4bf-111">-DefaultProfile</span></span>
<span data-ttu-id="df4bf-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="df4bf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df4bf-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df4bf-113">-InputObject</span></span>
<span data-ttu-id="df4bf-114">Serverobjektet som ska användas med åtgärden för avancerad skydds policy</span><span class="sxs-lookup"><span data-stu-id="df4bf-114">The server object to use with Advanced Threat Protection policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df4bf-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df4bf-115">-ResourceGroupName</span></span>
<span data-ttu-id="df4bf-116">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="df4bf-116">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df4bf-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="df4bf-117">-ServerName</span></span>
<span data-ttu-id="df4bf-118">Server namn för SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="df4bf-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="df4bf-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="df4bf-119">-Confirm</span></span>
<span data-ttu-id="df4bf-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="df4bf-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4bf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df4bf-121">-WhatIf</span></span>
<span data-ttu-id="df4bf-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="df4bf-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="df4bf-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="df4bf-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4bf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df4bf-124">CommonParameters</span></span>
<span data-ttu-id="df4bf-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df4bf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df4bf-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df4bf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df4bf-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="df4bf-127">INPUTS</span></span>

### <span data-ttu-id="df4bf-128">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="df4bf-128">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>
<span data-ttu-id="df4bf-129">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="df4bf-129">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="df4bf-130">System. String</span><span class="sxs-lookup"><span data-stu-id="df4bf-130">System.String</span></span>

## <span data-ttu-id="df4bf-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="df4bf-131">OUTPUTS</span></span>

### <span data-ttu-id="df4bf-132">Microsoft. Azure. commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="df4bf-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="df4bf-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="df4bf-133">NOTES</span></span>

## <span data-ttu-id="df4bf-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="df4bf-134">RELATED LINKS</span></span>
