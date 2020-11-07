---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: c8a3e10fb2f78556112831f4310eca60e296cf48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758264"
---
# <span data-ttu-id="cb6df-101">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="cb6df-101">Set-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="cb6df-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cb6df-102">SYNOPSIS</span></span>
<span data-ttu-id="cb6df-103">Ändrar en brand Väggs regel i Azure SQL Database Server.</span><span class="sxs-lookup"><span data-stu-id="cb6df-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb6df-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cb6df-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb6df-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cb6df-105">DESCRIPTION</span></span>
<span data-ttu-id="cb6df-106">Cmdleten **set-AzureRmSqlServerFirewallRule** ändrar en brand Väggs regel i en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="cb6df-106">The **Set-AzureRmSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="cb6df-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cb6df-107">EXAMPLES</span></span>

### <span data-ttu-id="cb6df-108">Exempel 1: ändra en brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="cb6df-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="cb6df-109">Det här kommandot ändrar en brand Väggs regel som heter Rule01 på den server som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="cb6df-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="cb6df-110">Kommandot ändrar Start-och slut-IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="cb6df-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="cb6df-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cb6df-111">PARAMETERS</span></span>

### <span data-ttu-id="cb6df-112">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="cb6df-112">-EndIpAddress</span></span>
<span data-ttu-id="cb6df-113">Anger slutvärdet för IP-adressintervallet för den här regeln.</span><span class="sxs-lookup"><span data-stu-id="cb6df-113">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb6df-114">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="cb6df-114">-FirewallRuleName</span></span>
<span data-ttu-id="cb6df-115">Anger namnet på brand Väggs regeln som ändras av den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cb6df-115">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb6df-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb6df-116">-ResourceGroupName</span></span>
<span data-ttu-id="cb6df-117">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="cb6df-117">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="cb6df-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cb6df-118">-ServerName</span></span>
<span data-ttu-id="cb6df-119">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="cb6df-119">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb6df-120">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="cb6df-120">-StartIpAddress</span></span>
<span data-ttu-id="cb6df-121">Anger startvärdet för IP-adressintervallet för brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="cb6df-121">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb6df-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cb6df-122">-Confirm</span></span>
<span data-ttu-id="cb6df-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cb6df-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb6df-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb6df-124">-WhatIf</span></span>
<span data-ttu-id="cb6df-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cb6df-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb6df-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cb6df-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb6df-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb6df-127">-DefaultProfile</span></span>
<span data-ttu-id="cb6df-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cb6df-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb6df-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb6df-129">CommonParameters</span></span>
<span data-ttu-id="cb6df-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb6df-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb6df-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb6df-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb6df-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cb6df-132">INPUTS</span></span>

## <span data-ttu-id="cb6df-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cb6df-133">OUTPUTS</span></span>

### <span data-ttu-id="cb6df-134">Microsoft. Azure. commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="cb6df-134">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="cb6df-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cb6df-135">NOTES</span></span>

## <span data-ttu-id="cb6df-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cb6df-136">RELATED LINKS</span></span>

[<span data-ttu-id="cb6df-137">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="cb6df-137">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="cb6df-138">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="cb6df-138">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="cb6df-139">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="cb6df-139">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="cb6df-140">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="cb6df-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


