---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveradvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedThreatProtection.md
ms.openlocfilehash: d6a06c3f4c50e10522ed06e6b1cd4185c1ef6768
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746785"
---
# <span data-ttu-id="7f2d1-101">Disable-AzSqlServerAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="7f2d1-101">Disable-AzSqlServerAdvancedThreatProtection</span></span>

## <span data-ttu-id="7f2d1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7f2d1-102">SYNOPSIS</span></span>
<span data-ttu-id="7f2d1-103">Inaktiverar Avancerat skydd på en server.</span><span class="sxs-lookup"><span data-stu-id="7f2d1-103">Disables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="7f2d1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7f2d1-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedThreatProtection [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7f2d1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7f2d1-105">DESCRIPTION</span></span>
<span data-ttu-id="7f2d1-106">Cmdleten **disable-AzSqlServerAdvancedThreatProtection** inaktiverar Avancerat skydd mot en server.</span><span class="sxs-lookup"><span data-stu-id="7f2d1-106">The **Disable-AzSqlServerAdvancedThreatProtection** cmdlet disables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="7f2d1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7f2d1-107">EXAMPLES</span></span>

### <span data-ttu-id="7f2d1-108">Exempel 1 – inaktivera Avancerat skydd för Server</span><span class="sxs-lookup"><span data-stu-id="7f2d1-108">Example 1 - Disable server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedThreatProtection `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="7f2d1-109">Exempel 2 – inaktivera Avancerat skydd för Server från Server resurs</span><span class="sxs-lookup"><span data-stu-id="7f2d1-109">Example 2 - Disable server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedThreatProtection

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="7f2d1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7f2d1-110">PARAMETERS</span></span>

### <span data-ttu-id="7f2d1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f2d1-111">-DefaultProfile</span></span>
<span data-ttu-id="7f2d1-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7f2d1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f2d1-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f2d1-113">-InputObject</span></span>
<span data-ttu-id="7f2d1-114">Serverobjektet som ska användas med åtgärden för avancerad skydds policy</span><span class="sxs-lookup"><span data-stu-id="7f2d1-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="7f2d1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f2d1-115">-ResourceGroupName</span></span>
<span data-ttu-id="7f2d1-116">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7f2d1-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="7f2d1-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7f2d1-117">-ServerName</span></span>
<span data-ttu-id="7f2d1-118">Server namn för SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="7f2d1-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="7f2d1-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7f2d1-119">-Confirm</span></span>
<span data-ttu-id="7f2d1-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7f2d1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f2d1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f2d1-121">-WhatIf</span></span>
<span data-ttu-id="7f2d1-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7f2d1-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7f2d1-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7f2d1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f2d1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f2d1-124">CommonParameters</span></span>
<span data-ttu-id="7f2d1-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f2d1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f2d1-126">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f2d1-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f2d1-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7f2d1-127">INPUTS</span></span>

### <span data-ttu-id="7f2d1-128">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="7f2d1-128">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="7f2d1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7f2d1-129">System.String</span></span>

## <span data-ttu-id="7f2d1-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7f2d1-130">OUTPUTS</span></span>

### <span data-ttu-id="7f2d1-131">Microsoft. Azure. commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="7f2d1-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="7f2d1-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7f2d1-132">NOTES</span></span>

## <span data-ttu-id="7f2d1-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7f2d1-133">RELATED LINKS</span></span>
