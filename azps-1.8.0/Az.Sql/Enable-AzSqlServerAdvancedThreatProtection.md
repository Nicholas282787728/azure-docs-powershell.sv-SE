---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlserveradvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedThreatProtection.md
ms.openlocfilehash: aaaf417137bb1ec16150a2bf3d0ac88b64e70fae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746783"
---
# <span data-ttu-id="f49b6-101">Enable-AzSqlServerAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="f49b6-101">Enable-AzSqlServerAdvancedThreatProtection</span></span>

## <span data-ttu-id="f49b6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f49b6-102">SYNOPSIS</span></span>
<span data-ttu-id="f49b6-103">Aktiverar Avancerat skydd på en server.</span><span class="sxs-lookup"><span data-stu-id="f49b6-103">Enables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="f49b6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f49b6-104">SYNTAX</span></span>

```
Enable-AzSqlServerAdvancedThreatProtection [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f49b6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f49b6-105">DESCRIPTION</span></span>
<span data-ttu-id="f49b6-106">Cmdleten **Enable-AzSqlServerAdvancedThreatProtection** aktiverar Avancerat skydd på en server.</span><span class="sxs-lookup"><span data-stu-id="f49b6-106">The **Enable-AzSqlServerAdvancedThreatProtection** cmdlet enables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="f49b6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f49b6-107">EXAMPLES</span></span>

### <span data-ttu-id="f49b6-108">Exempel 1-aktivera avancerat skydd för Server</span><span class="sxs-lookup"><span data-stu-id="f49b6-108">Example 1 - Enable server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Enable-AzSqlServerAdvancedThreatProtection `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="f49b6-109">Exempel 2 – Aktivera server Avancerat skydd från Server resurs</span><span class="sxs-lookup"><span data-stu-id="f49b6-109">Example 2 - Enable server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Enable-AzSqlServerAdvancedThreatProtection

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="f49b6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f49b6-110">PARAMETERS</span></span>

### <span data-ttu-id="f49b6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f49b6-111">-DefaultProfile</span></span>
<span data-ttu-id="f49b6-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f49b6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f49b6-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f49b6-113">-InputObject</span></span>
<span data-ttu-id="f49b6-114">Serverobjektet som ska användas med åtgärden för avancerad skydds policy</span><span class="sxs-lookup"><span data-stu-id="f49b6-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="f49b6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f49b6-115">-ResourceGroupName</span></span>
<span data-ttu-id="f49b6-116">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f49b6-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="f49b6-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f49b6-117">-ServerName</span></span>
<span data-ttu-id="f49b6-118">Server namn för SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="f49b6-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="f49b6-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f49b6-119">-Confirm</span></span>
<span data-ttu-id="f49b6-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f49b6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f49b6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f49b6-121">-WhatIf</span></span>
<span data-ttu-id="f49b6-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f49b6-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f49b6-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f49b6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f49b6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f49b6-124">CommonParameters</span></span>
<span data-ttu-id="f49b6-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f49b6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f49b6-126">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f49b6-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f49b6-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f49b6-127">INPUTS</span></span>

### <span data-ttu-id="f49b6-128">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="f49b6-128">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="f49b6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f49b6-129">System.String</span></span>

## <span data-ttu-id="f49b6-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f49b6-130">OUTPUTS</span></span>

### <span data-ttu-id="f49b6-131">Microsoft. Azure. commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="f49b6-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="f49b6-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f49b6-132">NOTES</span></span>

## <span data-ttu-id="f49b6-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f49b6-133">RELATED LINKS</span></span>
