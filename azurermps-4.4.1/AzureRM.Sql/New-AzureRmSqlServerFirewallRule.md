---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 51AF8EFB-F0C1-41E0-BBC5-E48FB1B8672C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: b40ac97f5658758fa77900dfc31da5f77fb5d0e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755417"
---
# <span data-ttu-id="f3bb7-101">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f3bb7-101">New-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="f3bb7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f3bb7-102">SYNOPSIS</span></span>
<span data-ttu-id="f3bb7-103">Skapar en brand Väggs regel för en SQL-databasserver.</span><span class="sxs-lookup"><span data-stu-id="f3bb7-103">Creates a firewall rule for a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3bb7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f3bb7-104">SYNTAX</span></span>

### <span data-ttu-id="f3bb7-105">UserSpecifiedRuleSet</span><span class="sxs-lookup"><span data-stu-id="f3bb7-105">UserSpecifiedRuleSet</span></span>
```
New-AzureRmSqlServerFirewallRule -FirewallRuleName <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3bb7-106">AzureIpRuleSet</span><span class="sxs-lookup"><span data-stu-id="f3bb7-106">AzureIpRuleSet</span></span>
```
New-AzureRmSqlServerFirewallRule [-AllowAllAzureIPs] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3bb7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f3bb7-107">DESCRIPTION</span></span>
<span data-ttu-id="f3bb7-108">Cmdleten **New-AzureRmSqlServerFirewallRule** skapar en brand Väggs regel för den angivna Azure SQL Database-servern.</span><span class="sxs-lookup"><span data-stu-id="f3bb7-108">The **New-AzureRmSqlServerFirewallRule** cmdlet creates a firewall rule for the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="f3bb7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f3bb7-109">EXAMPLES</span></span>

### <span data-ttu-id="f3bb7-110">Exempel 1: skapa en brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="f3bb7-110">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.198" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.198
EndIpAddress      : 192.168.0.199
FirewallRuleName  : Rule01
```

<span data-ttu-id="f3bb7-111">Det här kommandot skapar en brand Väggs regel med namnet Rule01 på den server som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="f3bb7-111">This command creates a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="f3bb7-112">Regeln inkluderar angivna start-och slut-IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="f3bb7-112">The rule includes the specified start and end IP addresses.</span></span>

### <span data-ttu-id="f3bb7-113">Exempel 2: skapa en brand Väggs regel som gör att alla Azure IP-adresser kan komma åt servern</span><span class="sxs-lookup"><span data-stu-id="f3bb7-113">Example 2: Create a firewall rule that allows all Azure IP addresses to access the server</span></span>
```
PS C:\>New-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AllowAllAzureIPs
```

<span data-ttu-id="f3bb7-114">Det här kommandot skapar en brand Väggs regel på servern med namnet Server01 som tillhör resurs gruppen med namnet ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="f3bb7-114">This command creates a firewall rule on the server named Server01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="f3bb7-115">Eftersom parametern *AllowAllAzureIPs* används tillåter brand Väggs regeln alla Azure IP-adresser att nå servern.</span><span class="sxs-lookup"><span data-stu-id="f3bb7-115">Since the *AllowAllAzureIPs* parameter is used, the firewall rule allows all Azure IP addresses to access the server.</span></span>

## <span data-ttu-id="f3bb7-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f3bb7-116">PARAMETERS</span></span>

### <span data-ttu-id="f3bb7-117">-AllowAllAzureIPs</span><span class="sxs-lookup"><span data-stu-id="f3bb7-117">-AllowAllAzureIPs</span></span>
<span data-ttu-id="f3bb7-118">Visar att den här brand Väggs regeln tillåter att alla Azure IP-adresser får åtkomst till servern.</span><span class="sxs-lookup"><span data-stu-id="f3bb7-118">Indicates that this firewall rule allows all Azure IP addresses to access the server.</span></span>
<span data-ttu-id="f3bb7-119">Du kan inte använda den här parametern om du tänker använda parametrarna *FirewallRuleName* , *StartIpAddress* och *EndIpAddress* .</span><span class="sxs-lookup"><span data-stu-id="f3bb7-119">You cannot use this parameter if you intend to use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>
<span data-ttu-id="f3bb7-120">Om du vill tillåta att Azure IP-adresser får åtkomst till servern ska denna parameter användas i ett separat cmdlet-anrop som inte använder parametrarna *FirewallRuleName* , *StartIpAddress* och *EndIpAddress* .</span><span class="sxs-lookup"><span data-stu-id="f3bb7-120">If you want to allow Azure IPs to access the server, this parameter should be used in a separate cmdlet call that does not use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureIpRuleSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3bb7-121">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="f3bb7-121">-EndIpAddress</span></span>
<span data-ttu-id="f3bb7-122">Anger slutvärdet för IP-adressintervallet för den här regeln.</span><span class="sxs-lookup"><span data-stu-id="f3bb7-122">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3bb7-123">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="f3bb7-123">-FirewallRuleName</span></span>
<span data-ttu-id="f3bb7-124">Anger namnet på den nya brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="f3bb7-124">Specifies the name of the new firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3bb7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3bb7-125">-ResourceGroupName</span></span>
<span data-ttu-id="f3bb7-126">Anger namnet på en resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="f3bb7-126">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="f3bb7-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f3bb7-127">-ServerName</span></span>
<span data-ttu-id="f3bb7-128">Anger namnet på en server.</span><span class="sxs-lookup"><span data-stu-id="f3bb7-128">Specifies the name of a server.</span></span>
<span data-ttu-id="f3bb7-129">Ange Server namnet, inte det fullständigt kvalificerade DNS-namnet.</span><span class="sxs-lookup"><span data-stu-id="f3bb7-129">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="f3bb7-130">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="f3bb7-130">-StartIpAddress</span></span>
<span data-ttu-id="f3bb7-131">Anger startvärdet för IP-adressintervallet för brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="f3bb7-131">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3bb7-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f3bb7-132">-Confirm</span></span>
<span data-ttu-id="f3bb7-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f3bb7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3bb7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3bb7-134">-WhatIf</span></span>
<span data-ttu-id="f3bb7-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f3bb7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3bb7-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f3bb7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3bb7-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3bb7-137">-DefaultProfile</span></span>
<span data-ttu-id="f3bb7-138">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f3bb7-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3bb7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3bb7-139">CommonParameters</span></span>
<span data-ttu-id="f3bb7-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3bb7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3bb7-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3bb7-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3bb7-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f3bb7-142">INPUTS</span></span>

## <span data-ttu-id="f3bb7-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f3bb7-143">OUTPUTS</span></span>

### <span data-ttu-id="f3bb7-144">Microsoft. Azure. commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="f3bb7-144">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="f3bb7-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f3bb7-145">NOTES</span></span>

## <span data-ttu-id="f3bb7-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f3bb7-146">RELATED LINKS</span></span>

[<span data-ttu-id="f3bb7-147">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f3bb7-147">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="f3bb7-148">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f3bb7-148">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="f3bb7-149">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f3bb7-149">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="f3bb7-150">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="f3bb7-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


