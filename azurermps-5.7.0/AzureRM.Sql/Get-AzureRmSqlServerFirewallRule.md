---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: eb514075bd366a0360f29c65455805be5f85569f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573192"
---
# <span data-ttu-id="8e9a5-101">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8e9a5-101">Get-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="8e9a5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8e9a5-102">SYNOPSIS</span></span>
<span data-ttu-id="8e9a5-103">Hämtar brand Väggs regler för en SQL-databasserver.</span><span class="sxs-lookup"><span data-stu-id="8e9a5-103">Gets firewall rules for a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e9a5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8e9a5-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e9a5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8e9a5-105">DESCRIPTION</span></span>
<span data-ttu-id="8e9a5-106">Cmdleten **Get-AzureRmSqlServerFirewallRule** hämtar brand Väggs regler för en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="8e9a5-106">The **Get-AzureRmSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="8e9a5-107">Om du anger namnet på en brand Väggs regel får denna cmdlet information om den specifika brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="8e9a5-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="8e9a5-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8e9a5-108">EXAMPLES</span></span>

### <span data-ttu-id="8e9a5-109">Exempel 1: Hämta alla regler för en server</span><span class="sxs-lookup"><span data-stu-id="8e9a5-109">Example 1: Get all rules for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName : ResourceGroup01
ServerName        : server01
StartIpAddress    : 0.0.0.0
EndIpAddress      : 0.0.0.0
FirewallRuleName  : AllowAllWindowsAzureIps

ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 1.2.3.4
EndIpAddress      : 4.3.2.1
FirewallRuleName  : Rule01
```

<span data-ttu-id="8e9a5-110">Det här kommandot får alla brand Väggs regler för servern som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="8e9a5-110">This command gets all the firewall rules for the server named Server01.</span></span>

## <span data-ttu-id="8e9a5-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8e9a5-111">PARAMETERS</span></span>

### <span data-ttu-id="8e9a5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e9a5-112">-DefaultProfile</span></span>
<span data-ttu-id="8e9a5-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8e9a5-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e9a5-114">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="8e9a5-114">-FirewallRuleName</span></span>
<span data-ttu-id="8e9a5-115">Anger namnet på brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="8e9a5-115">Specifies the name of the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e9a5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e9a5-116">-ResourceGroupName</span></span>
<span data-ttu-id="8e9a5-117">Anger namnet på den resurs grupp som SQL-servern har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="8e9a5-117">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e9a5-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8e9a5-118">-ServerName</span></span>
<span data-ttu-id="8e9a5-119">Anger namnet på SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8e9a5-119">Specifies the name of the SQL Server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e9a5-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8e9a5-120">-Confirm</span></span>
<span data-ttu-id="8e9a5-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8e9a5-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e9a5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e9a5-122">-WhatIf</span></span>
<span data-ttu-id="8e9a5-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8e9a5-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e9a5-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8e9a5-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e9a5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e9a5-125">CommonParameters</span></span>
<span data-ttu-id="8e9a5-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e9a5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e9a5-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e9a5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e9a5-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8e9a5-128">INPUTS</span></span>

### <span data-ttu-id="8e9a5-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="8e9a5-129">None</span></span>
<span data-ttu-id="8e9a5-130">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="8e9a5-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8e9a5-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8e9a5-131">OUTPUTS</span></span>

### <span data-ttu-id="8e9a5-132">Microsoft. Azure. commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="8e9a5-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="8e9a5-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8e9a5-133">NOTES</span></span>

## <span data-ttu-id="8e9a5-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8e9a5-134">RELATED LINKS</span></span>

[<span data-ttu-id="8e9a5-135">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8e9a5-135">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="8e9a5-136">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8e9a5-136">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="8e9a5-137">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8e9a5-137">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="8e9a5-138">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="8e9a5-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


